# Day 4 - Permissions and Ownership (Part 1)

split day 4 into 2 parts today covered the basics saving the tricky stuff (SUID, SGID, sticky bit, sudoers) for part 2.

## rwx meaning
r/w/x means something different on a file vs a directory. on a file its straightforward  read, write, execute.
on a directory though x actually means traverse/access, took me a moment to get that.

## file vs directory permissions
directory permission controls access to the path itself 
file permission controls what you can actually do with the file read it, edit it, run it.

## owner, group, others
three classes decide who a permission applies to  the owner, the group, and everyone else (others).

## chmod
two ways to use it:
- numeric - like 755, 644
- symbolic - using u, g, o with +, -, =

## chown
changes the owner of a file or owner + group together

## chgrp
only changes the group ownership nothing else

## recursive with -R
applies the change to the whole directory tree at once

## Skipped today
- SUID - parked, the concept didnt click today not skipped permanently coming back to it
- SGID
- sticky bit
- sudoers/visudo
- least privilege
- permission troubleshooting

## Plan for part 2
not repeating SUID theory, doing it practical this time with real use cases 
order SUID, SGID, sticky bit, then sudo/sudoers, least privilege, troubleshooting scenarios, then a strict test permissions chapter closes after that.
