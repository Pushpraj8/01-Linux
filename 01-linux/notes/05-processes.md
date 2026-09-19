# Day 5 — Processes (Part 1)

## what is a process
a running program is called a process. when you run a command it loads into memory and starts running. that running instance is a process.

## program vs process
- program = file on disk (static)
- process = running instance in memory (dynamic)
- one program can have multiple processes

## PID
- every process has a unique number
- PID 1 = systemd (created at boot)
- when process ends, PID is freed

## PPID
- parent process id
- any command you run in terminal, its parent = bash
- PID 1 has no parent

## process states

| state | meaning |
|-------|---------|
| R | running / runnable |
| S | sleeping (normal waiting) |
| D | io wait |
| Z | zombie |

- in `Ss`, S = state, lowercase s = session leader (just awareness)
- `R+` = running + foreground
- S is the most common state - normal waiting
- D process cannot be killed easily
- Z = process dead but parent has not read exit status

## zombie
zombie process means - the process is dead but its parent has not read its exit status. so it stays in Z state. for this we need to investigate the parent, not the zombie.

## commands used
- `echo $$` - my bash PID
- `ps` - processes in current terminal
- `ps aux` - all processes
- `ps aux | head -5` - top 5
- `ps aux | grep pushpraj` - my processes
- `pstree -p` - process tree
- `ps -o pid,ppid,stat,cmd` - with states
- `sleep 120 &` - sleep in background

## observations
- PID 1 = systemd, USER = root
- `[kthreadd]` = kernel thread (in brackets)
- `avahi` = system user, not a normal user
- grep itself becomes a process
- pipewire, dbus = desktop background services

## what i learned
- every command creates a process when it runs
- not just applications - ls, grep, ps too
- bash is my parent
- commands are not to be memorized, they are to be written in notes
- S state is normal, not bad

## pending (day 5 part 2)
- ps aux, ps -ef, pstree detailed
- top, htop
- pgrep, pidof
- &, jobs, ctrl+z, bg, fg
- kill, SIGTERM vs SIGKILL
- /proc/<PID>
- nohup, disown, screen/tmux
- production scenario
