# Commands — Lab 05

## bash pid
echo $$

## all processes
ps aux | head -5
ps aux | head -20

## my processes
ps aux | grep pushpraj

## find bash
ps aux | grep bash

## process tree
pstree -p

## check states
ps -o pid,ppid,stat,cmd

## sleep in bg
sleep 120 &
ps
