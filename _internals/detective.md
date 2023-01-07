the discover feed, as well as the advanced transparency report, make use of social graphs (web of trust) to compute their data.

This system runs in the background and is throttled based on existing server load (e.g., live reads take priority)

server load tracked by simple redis `incr` (but in the golang binary itself) - count the number of requests per second and reset each second - only run the job query if halfway offset from the second it's below `job_start_visits_limit`

the detective SQL queries need to be low impact
