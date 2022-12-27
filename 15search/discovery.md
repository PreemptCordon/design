basically, "find a subreddit", "people in X are often in Y"
- data here is dual opt-in:
	- being a recommended result is opt-in (whether you're discoverable)
	- data helping users to a result is opt-in
- ranking decisions are made by the searching user, based off how far away or near you want to be from something

the discovery search is slower because it's per-user ranked - it's a type of ranking, not a type of search (though a blank query is possible)

this is different from the site-configurable meter decisions

immediate sql or redis table or golang channels

- discovery template (a saved search)
	- template name
	- template settings
	- search results
	- re-run search
- distance factors:
	- weight: binary, linear, logarmithmic, exponential
	- direction: positive, negative
- enemies: (cannot select enemies only inclusion filter, this is only an exclusion filter)
	- blocked by me
	- blocked by them
	- distance factor (avoid encounters)
- friends:
	- delegates to me
	- delegated by me
	- distance factor (get outside comfort zone)
- specific tag
	- direction (exclude/include)
	- zombie distance factor
- hazard avoidance
	- not unanimous, healthy amount of dissent recorded
	- sorted by least-agreement
	- prevent returning result that mostly agrees with somone they've blocked (it could get ugly)
		- this is for preventing brigading
	- invite-only system
		- affect inviter's karma if abused
	- rate-limited token bucket
		- rate limit for discover must be approved by site admins
