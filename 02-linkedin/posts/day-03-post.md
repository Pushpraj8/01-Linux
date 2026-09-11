day 3 done.

todays topic was users and groups, UID and GID are just numbers, one for user one for group UID 0 is root, remembered that one easily.

spent a while on /etc/passwd file, its got 7 fields separated by colons theres this one field GECOS that just wont stick in my head, dont know why
its just some description field, nothing to do with groups but the name confuses me every time 

the thing that actually clicked was primary vs supplementary groups. every user has one primary group from /etc/passwd but can be part of other groups too, 
those extra ones are supplementary saw an actual example and that made way more sense than just the definition

didnt touch /etc/shadow deeply, keeping that for later when security stuff comes up 

tomorrow is heavier - useradd, usermod, userdel, groupadd, and whats actually happening behind the scenes when you create a user. plus the test at the end

github: https://github.com/Pushpraj8/01-linux

