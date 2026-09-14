# Lab 04 - Permissions & Ownership

## What I did
Practiced basic permissions today - chmod (numeric and symbolic), chown, chgrp created a test file and directory, checked their default permissions, then changed them to see how rwx behaves on files vs directories also changed file ownership to root and back, and tried changing group ownership with a test group.

## What went wrong
chown and chgrp needed sudo - got permission denied first time also, before this lab i used to think chmod 755 on a directory and on a file mean the same thing, but they don't nn a directory, x means "traverse into it", not "execute" had to re-read that part.

## How I fixed it
Used sudo for chown/chgrp 
For the directory thing, I actually created a test dir, removed x permission, and tried to cd into it got "Permission denied" that cleared up the difference real quick

## What I learned
- chmod 755 = rwxr-xr-x, chmod 644 = rw-r--r--
- On a file: r = read, w = write, x = execute (run the file)
- On a directory: r = list contents, w = create/delete files inside, x = traverse into it
- Without x on a directory, you can't cd into it even if you have r
- chown changes owner, chgrp changes group - both need sudo
- Format: chown user:group file
- Symbolic chmod (u+x, g-w) is easier to read than numeric sometimes
