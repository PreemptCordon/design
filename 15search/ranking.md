search results are ranked according to the user's preference in the search menu:

1. feed-style ranking (good for articles, bad for comments)
2. comment-style ranking (no preference for first-comments)
3. discover-style ranking (takes longer and can only do one at a time per user)

- ranking includes an automatic demote for reported posts (mods can undo that when they open the report)
	- transparency report (ran twice with and without deranking)
		- show category/reason and amount
- automatic demote for link aggregation (unpinterested)

## old notes
### comment sort
- [ ] comments wilson score interval (not percent up/down but number up/down, exclude/include muted/delegated)
- reddit post algorithm and the reddit comment algorithm are different - the comment algorithm doesn't have a bias to new/first comments
```python
# Rewritten code from /r2/r2/lib/db/_sorts.pyx
from math import sqrt

def _confidence(ups, downs):
    n = ups + downs

    if n == 0:
        return 0

    z = 1.281551565545
    p = float(ups) / n

    left = p + 1/(2*n)*z*z
    right = z*sqrt(p*(1-p)/n + z*z/(4*n*n))
    under = 1+1/n*z*z

    return (left - right) / under

def confidence(ups, downs):
    if ups + downs == 0:
        return 0
    else:
        return _confidence(ups, downs)
```


### feed sort
- YC's algorithm for ranking = (points - 1) / (hours + 2) ^1.5
- [ ] ranking (slashdot oligarch groupthink -1 to 5, account age/karma), post age,
- [ ] vote ranking: logmarithmic (first votes bigger bump), age items slowly
- [ ] ranking: votes/time(no bumping), location/proximity

```python
# https://medium.com/hacking-and-gonzo/how-reddit-ranking-algorithms-work-ef111e33d0d9
# Rewritten code from /r2/r2/lib/db/_sorts.pyx

from datetime import datetime, timedelta
from math import log

epoch = datetime(1970, 1, 1)

def epoch_seconds(date):
    td = date - epoch
    return td.days * 86400 + td.seconds + (float(td.microseconds) / 1000000)

def score(ups, downs):
    return ups - downs

def hot(ups, downs, date):
    s = score(ups, downs)
    order = log(max(abs(s), 1), 10)
    sign = 1 if s > 0 else -1 if s < 0 else 0
    seconds = epoch_seconds(date) - 1134028003
    return round(sign * order + seconds / 45000, 7)
```

