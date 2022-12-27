choices are templates for decisions

decisions are composed of options, and users react with selections

choices are some kind of yaml frontmatter (a subdialect allowing parsing into the database)

choices don't have due dates, decisions do
choices link to a wiki article explaining how they work and how you should build a decision

choice style
- minimum bar for petition to be considered (based on choice type)
choice templates are basically toml/yaml and are exchangable/saveable
actual decision gets rendered (@@group -> @@group#timestamp @@wiki#version)
- decisions have a vote type
	- concensus-unanimous
	- compromise-rcv
	- lazy-concensus
	- threshold
