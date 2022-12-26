# design
Design notes for Preempt Cordon
> todo: add graphic of 2 helix's then split to the various ideas (abilene paradox/tactical voting)

> "A fediverse site for having arguments on the internet, without spending all your time having arguments on the internet"

- decide things
	- create choices (templates for decision flow)
	- open individual decisions (allow proposing options)
	- propose options
	- discuss options along facets in wiki-format
	- make selections
- vote or delegate power (liquid democracy)
	- consensus-unanimus (for core things without time limits)
	- compromise-rcv (for debatable options)
	- lazy-concensus (for light edits/effort-based)
	- threshold-approval (for immediate ugent actions)
- maintain reputation/karma
	- actual choice selection doesn't impact karma
	- argumentative points impact karma
	- observer (non-participating) members can still affect karma
	- meta-moderation / failing to complete role duties
- user-controlled algorithms
	- feed
	- comments
	- search
	- discovery
	- decisions

- why?
	- abilene paradox, tactical voting, duvergers law
	- gridlock, ineffective committees, direct voting
	- collective illusions, better feedback
	- trust, delegation
	- drama, algorithms,
	- choice, agency
- why not
	- underlying problem is almost always social, not technical
	- software doesn't fix problems, action does
- problems/prizes
	- jude wanniski two santa claus theory
	- permanent fixes not dog chasing car
	- strain theory
	- itterative game theory with reputation
	- discontinuity effect
	- 

#todo
- accounts
	- [ ] registration, sign in, sign out, recovery, deletion
- documents/wiki
	- [ ] section versioning
	- [ ] per-section editors
	- [ ] parent category
	- [ ] managing group
	- [ ] approval process trigger
	- [ ] sections can be programatic (like specific modications)
		- [ ] old objects don't immediately use new logic
- groups
	- [ ] group memberships
	- [ ] tag/category ownership
	- [ ] subgroups (via ownership of subcategory)
	- [ ] visibility vs decision reactions (decision to report a post is site-wide enabled)
- vote
	- wiki links
		- [ ] overall process document
		- [ ] this specific decision
			- [ ] wiki links to option proposals
		- [ ] wiki links to axis/facet considerations
			- [ ] links to counter proposal rating of each facet
	- vote styles
		- [ ] concensus-unanimous
		- [ ] compromise-RCV
		- [ ] lazy-apache
		- [ ] threshold (2-man-rule) - inverse concensus
	- option adding
		- [ ] group allowed to add options
		- [ ] options are sections (per section authors can be groups)
		- [ ] minimum threshold for option to be added (similar to draft)
		- [ ] mod approval of option-delegation threshhold
		- [ ] section in-group edit approval, requires concensus approval from other option groups (meaning has changed) or threshold from admins (if votes have already started)
		- [ ] if option approves a specific trigger change
	- user selections
		- [ ] RCV
	- decision composition
		- [ ] pick mod group of election
		- [ ] pick option proposing group
		- [ ] pick voting proposing group
		- [ ] link to wikis
		- [ ] deadline
		- [ ] next action (enable/disable)
	- decision type templating
		- [ ] flow design
		- [ ] process wiki
- mod
	- [ ] mod decision trees (report buttons trigger votes)
		- [ ] prevent users from preventing report vote?
		- [ ] preemptive actions
			- [ ] downrank/hide
			- [ ] ignores (for users that are reported repeatedly maliciously)
			- [ ] preserve S3 / prevent deletion of specific content
			- [ ] rate limit enable
		- [ ] process document for the specific report
		- [ ] notification flow (disabled/delayed, immediate, vague)
		- [ ] votes for this decision
		- [ ] enabled action (remove privileges, remove content, )
		- [ ] user appeal process
	- rate limits
		- [ ] link detection auto-ratelimit
		- [ ] frequently-edited document auto-ratelimit
		- [ ] invite rate limit
- search
	- [ ] obey per-post privacy
	- [ ] obey blocks
	- [ ] don't include drafts
	- [ ] scope distance (to semantic tags)
- feed
	- [ ] RSS
	- [ ] email notifications
	- [ ] browser notifications
	- [ ] user-configured ranking (feed vs comments)
- user-configured discovery (slower than search)
	- [ ] opt-in community/user visibility
	- [ ] opt-in preference considerations
	- [ ] similarity proximity filters
	- [ ] mod hazard alarm (if filtering to enemy groups and then causing a lot of mod activity)
- cryptography
	- [ ] private votes (via private group membership/ring cryptography) - why? allow people to be who they really are (collective illusion problem)
		- [ ] edits/proposals aren't private (since they do more damage than votes)
		- [ ] delegation isn't private (the zombies are, the representative isn't)


#todo 
https://github.com/sagikazarmark/modern-go-application
https://github.com/eapache/go-resiliency
https://github.com/teivah/100-go-mistakes
https://github.com/TheAlgorithms/Python/blob/master/DIRECTORY.md
https://github.com/TheAlgorithms/Go
https://google.github.io/styleguide/go/decisions
https://google.github.io/styleguide/go/guide
https://google.github.io/styleguide/pyguide.html
https://google.github.io/styleguide/go/best-practices
https://github.com/charmbracelet/charm/tree/main/server
https://teivah.medium.com/maps-and-memory-leaks-in-go-a85ebe6e7e69
https://tanveerprottoy.medium.com/structuring-go-application-in-a-modular-way-5eb8f8359683
http://marcio.io/2015/07/handling-1-million-requests-per-minute-with-golang/
https://itnext.io/build-grpc-server-with-golang-go-step-by-step-b3f5abcf9e0e
https://courses.calhoun.io/courses/cor_gophercises
https://www.alexedwards.net/blog/working-with-cookies-in-go
https://www.alexedwards.net/blog/which-go-router-should-i-use
https://arslan.io/2022/12/04/functional-table-driven-tests-in-go/
https://zotlabs.org/page/zot/specs+zot6+messages
https://codeberg.org/streams/streams
https://dev.to/llance_24/golang-csrf-defense-in-practice-10k