# Commands - Lab 03 Users & Groups

## Current user info
whoami
id
groups

## System files
head -5 /etc/passwd
head -5 /etc/group

## User create
sudo useradd -m testuser1

## Verify
id testuser1
grep testuser1 /etc/passwd
grep testuser1 /etc/group

## Cleanup
sudo userdel -r testuser1
