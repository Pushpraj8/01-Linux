# Lab 05 — Processes

## What I did
today i learned about processes. checked my bash pid with echo $$ and got 7703. then ran ps aux to see all processes. ran sleep 120 & in background and checked with ps - it was in S state. used pstree to see the tree. also looked at process states R S D Z.

## What went wrong
at first i thought only applications like firefox make processes. but when i ran ps aux i saw ls grep ps - all of them were processes too. took me some time to understand this. S state was also confusing at first. i thought S means process is stuck but later understood S is just normal waiting. most processes stay in S. zombie concept was also a bit confusing.

## How I fixed it
ran sleep 120 & and checked with ps. it was in S state because it was waiting for the time to finish. this made it clear that S is not a bad state. for zombie i understood that we need to check the parent not the zombie itself. realized grep also becomes a process which was funny at first.

## What I learned
every command creates a process when it runs. not just applications. PID is unique, PPID is parent's. bash is my parent. PID 1 is systemd. states are R running, S sleeping, D io wait, Z zombie. for zombie investigate parent not zombie. [kthreadd] in brackets means kernel threads.

## Part 2 — update

today looked at pstree top pgrep pidof and signals. `pstree -p` shows the tree structure. ran `top` which shows cpu memory and load. `pgrep -a chrome` shows pid with command details. `pidof chrome` gives only pid.

also looked at background process. ran `sleep 300 &`. got job number `[1]` and a pid too. understood both are different. did not go deep into jobs for now.

in signals looked at kill. SIGTERM `-15` is graceful, SIGKILL `-9` is forceful. should try -15 first, only use -9 if that does not work. -9 should not be the first choice.
