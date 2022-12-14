previously called "meters" or "meter decisions"

monitors evaluate selections & reactions, in the following ways:

- if delegated users haven't made a selection for a user, notify them to vote manually
- if reactions are enough to trigger a mod notification, notify mods
- when the decision time is up, trigger the actions of the option that won

these are circuitbreakers for issues. They're different from discovery (which is per user) and are meant for mods to keep things in control

- meter decisions do hook into votes & evaluate instantly (like the vote resolver)
	- they can hook into
		- trends of users
		- view count trends
		- edit trends
		- decision state trends (e.g. constantly blocked concensus)
		- decision result trends (e.g., unanimous decisions)
- types
	- based on reactions
		- alarm for controversy circuit breaker
			- e.g. engage crowd control
			- auto-demote overly interactive (slashdot alarm) - mods can manually override to allow it to keep spreading
		- a special exception is the moderator bully-victim search.
			- this pulls up cases where a particular user is being harrassed excessively by someone else.
			- cause/detection
				- constant negative voting (direct, not delegated)
				- alarm for brigading / robotic reaction
				- following people to disagree with them isn't allowed. participating in a group/team is fine though
			- actions
				- downrank enemy's ability to find them
	- based on votes
		- unanimity (group think) on RCV
			- cause/detection
				- not a lot of diversity in option choices
			- actions
				- engage wake-zombies
		- constant blockers on concensus
			- cause/detection
				- repeatedly blocked concensus
				- specific repeat user blocks concensus
			- actions
				- can mute to allow user to continue blocking concensus
				- can transition decision to RCV compromise
				- split group into subgroups (make more cohesive purpose/scope in their wikis)
		- lazy concensus constant debate raising
			- detection
				- a user's proposals constantly go into committee (simple sabotage guide)
				- a user is constantly reporting someone else
			- actions
				- demote reporting user from reporting role
				- demote proposing user from proposal role
				- ignore reporting user (for specific time) and let them keep doing it
				- ignore proposing user (for specific time) and let them keep doing it
	- user feedback of process reform
		- detections: users raise these (they're decision forms / contact forms)
			- not recognizing disent
			- shot down without alternative
			- manufactured consent (debate of process document or selected document raised)
			- vilifying others (CoC violation / recall of moderators)
		- actions
			- modify process documents
			- modify admin membership
- 