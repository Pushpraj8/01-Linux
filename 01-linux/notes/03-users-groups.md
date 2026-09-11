# Day 3 - users and groups

so today was about UID and GID, UID is just a number for the user, GID is the number for the group UID 0 = root, that one's important to remember.

whoami just shows current user. id shows UID, GID and all the groups you're in
groups command basically shows the same groups part alone.

then went into /etc/passwd file it has 7 fields separated by colons  username:x:UID:GID:GECOS:home:shell honestly got a bit confused at the 5th field, 
thought GECOS meant group but it's actually just a description thing not related to groups but the term itself keeps slipping out of my head. 

/etc/shadow has password stuff and expiry details.
didn't touch the detailed fields yet keeping that for later when security topics come properly.

/etc/group is simpler - group_name:x:GID:members

the part that actually made things click was primary vs supplementary groups
The primary group comes from the GID in /etc/passwd, but a user can also be part of other groups on top of that, those are supplementary
there was an example with a user rahul where his primary group was developers but he also had docker as a supplementary group, that made it way easier to understand

tomorrow's plan: useradd, passwd, usermod, userdel, groupadd, gpasswd, groupdel, /etc/skel, 
what changes when a user gets created, service users, and the day 3 test at the end.
