# Day 5 — Processes (Part 1)

## Process fundamentals
- Program vs Process
- PID (Process ID) — unique number
- PPID (Parent Process ID) — papa ka PID
- Parent → Child relationship
- PID 1 = systemd

## Process States

| State | Matlab |
|---|---|
| R | Running / Runnable |
| S | Sleeping (waiting for something) |
| D | Uninterruptible sleep (I/O wait) |
| Z | Zombie (dead, parent hasn't read exit status) |

- `Ss` me `S` = state, lowercase `s` = session leader
- `R+` = running, `+` = foreground
- `D` = disk/IO wait me atka, kill nahi ho sakta easily
- `Z` = zombie — parent ko investigate karna zaroori

## Practical commands used
- `sleep 120 &` — background me sleep chalao
- `ps`
- `ps -o pid,ppid,cmd`
- `ps -o pid,ppid,stat,cmd`

## Example — process tree

bash
├── sleep
└── ps


## What I learned
- Process states read karne aane chahiye
- Zombie ka matlab: process mar chuki, par parent ne uska exit status read nahi kiya
- `S` sabse common state hai — normal waiting

## Pending (Day 5 Part 2)
- `ps aux`, `ps -ef`, `pstree -p`
- `top`, `htop`
- `pgrep`, `pidof`
- `&`, `jobs`, `Ctrl+Z`, `bg`, `fg`
- `kill`, SIGTERM vs SIGKILL
- `/proc/<PID>`
- `nohup`, `disown`, `screen`/`tmux`
- Production scenario
