# Commands — Lab 05 Processes

## Bash PID
echo $$

## All processes
ps aux | head -5
ps aux | head -20

## My processes
ps aux | grep pushpraj

## Process tree
pstree -p

## PPID check
echo $$
ps -o pid,ppid,cmd -p $$

## Process states
ps -o pid,ppid,stat,cmd
