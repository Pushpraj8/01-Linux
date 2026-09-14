# Lab 03 — Users & Groups

## What I did
Practiced users and groups today. 
checked my own identity with whoami, id, groups looked at /etc/passwd and /etc/group to see how users are stored created a test user with useradd -m, verified it in both files, then deleted it with userdel -r.

## What went wrong
Nothing major useradd and userdel both needed sudo - got a permission denied first time because i forgot sudo.

## How I fixed it
Used sudo and it worked, realized these commands touch system files so they need root access by default.

## What i learned
- whoami shows current username, id shows UID/GID, groups shows all groups
- /etc/passwd has 7 fields separated by colons - username, password placeholder, UID, GID, GECOS, home dir, shell
- useradd -m creates a home directory automatically, without -m the home dir doesn't get created
- userdel -r removes the user and their home directory too
- These commands need sudo because they modify system files
