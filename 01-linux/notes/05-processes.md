# Day 5 — Processes (Part 1)

## process kya hai
running program ko process kehte hai. jab command chalate hai to memory me load hoti hai aur chalne lagti hai. us instance ko process kehte hai.

## program vs process
- program = disk pe padi file (static)
- process = memory me chal raha instance (dynamic)
- ek program ke multiple processes ho sakte hai

## PID
- har process ka unique number
- PID 1 = systemd (boot pe banta hai)
- process khatam to PID free

## PPID
- parent process id
- jo command terminal me chalao uska parent = bash
- PID 1 ka koi parent nahi

## process states

| state | matlab |
|-------|--------|
| R | running / runnable |
| S | sleeping (normal waiting) |
| D | io wait |
| Z | zombie |

- `Ss` me S = state, lowercase s = session leader (sirf awareness)
- `R+` = running + foreground
- S sabse common state hai - normal waiting
- D me process kill nahi ho sakta easily
- Z = process dead but parent ne exit status nahi padha

## zombie
zombie process ka matlab - process mar chuki hai par parent ne uska exit status read nahi kiya. isliye wo Z state me pada rehta hai. isme parent ko investigate karna hai zombie ko nahi.

## commands used
- `echo $$` - apna bash PID
- `ps` - current terminal ke processes
- `ps aux` - saare processes
- `ps aux | head -5` - top 5
- `ps aux | grep pushpraj` - apne processes
- `pstree -p` - process tree
- `ps -o pid,ppid,stat,cmd` - states ke saath
- `sleep 120 &` - background me sleep

## observations
- PID 1 = systemd, USER = root
- `[kthreadd]` = kernel thread (brackets me)
- `avahi` = system user, normal user nahi
- grep khud bhi process banta hai
- pipewire, dbus = desktop background services

## what i learned
- har command process banati hai jab chalti hai
- sirf applications nahi - ls, grep, ps bhi
- bash mera parent hai
- commands yaad nahi karne, notes me likhne hai
- S state normal hai, buri nahi

## pending (day 5 part 2)
- ps aux, ps -ef, pstree detailed
- top, htop
- pgrep, pidof
- &, jobs, ctrl+z, bg, fg
- kill, SIGTERM vs SIGKILL
- /proc/<PID>
- nohup, disown, screen/tmux
- production scenario
