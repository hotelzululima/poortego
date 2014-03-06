poortego
========

Latest iteration of poortego is a completely new code-base (the old ruby/metasploit code is under the poortego-ruby branch in case this ever wants to be revived).

This new iteration stems from the fun that I've had playing with neo4j and the natural way of traversing data (files) in the unix file-system as a way of traversing indicators. I'm using this for cyber threat indicators- but this framework could easily be used for managing other data points that are basic node/link data-types.

Current command interface/dispatcher is built ontop of python cmd2 and uses py2neo for neo4j REST communication.

The bare-bones commands work at present:
- help, exit, and namespace (standard)
- add and ln (wizards)
- cd, ls, pwd (traversals)
- session, storage, and user (information)
- purge

Roadmap
-------

Soon to come (1-2 weeks):
- additional argument support for bare-bones commands
- rm
- cat
- find
- man
- import/export (csv, json, mtgx, STIX, IOC, etc.)

Then:
- "transforms" (scripts to interact with data and create new nodes/linkages)
- "cron" (or "machines" in maltego lingo) to run/re-run scheduled transforms
- document retrieval (ala- curl/wget)
- raw document/file storage (link neo4j node to file-system path location)
-- maybe use a separate document storage solution (e.g., couchdb)

Later:
- Improved user/group/auth support (e.g., ldap)
- Better client/server support (ideally so little/no client-side requirements)
-- server API - REST/web, e.g., https://x.x.x.x/poortego.php?cmd=ls
- web interface / browser plug-in? (always preferred cli)
 

