# Lab 05 — Processes

## What I did
Practiced process fundamentals — checked bash PID with `echo $$`, listed all processes with `ps aux`, filtered my own processes, viewed process tree with `pstree -p`, and checked process states using `ps -o pid,ppid,stat,cmd`.

## What went wrong
At first I thought processes only come from applications like Firefox or Chrome. Didn't realize every command creates a process when it runs — even `ls`, `ps`, `grep`. Also confused `S` (sleeping) with stopped — later understood `S` is just normal waiting state, most processes are in `S` most of the time.

## How I fixed it
Ran `sleep 120 &` in the background and checked with `ps`. Saw its state change from `S` (sleeping) while waiting. Understood that states aren't about the process being broken — they just describe what it's doing right now.

## What I learned
- Every command creates a process
- PID = unique number, PPID = parent's PID
- PID 1 = systemd
- Process states: R (running), S (sleeping), D (I/O wait), Z (zombie)
- `Ss` = sleeping + session leader (lowercase `s` is just a flag)
- `R+` = running + foreground
- Zombie process = dead, but parent hasn't read its exit status
- In zombie case, investigate the parent, not the zombie itself
- `[kthreadd]` in brackets = kernel threads
