# Day 5 - Processes (Part 2)

## pstree -p
saw the parent child hierarchy practically. whatever command runs inside bash becomes its child. tree shows who is whose child.

## top
- shows cpu usage
- shows memory usage
- shows top resource consumer
- shows load average
- press q to exit

## pgrep
`pgrep -a chrome` - shows pid along with command details. not just pid, full command line shows.

## pidof
`pidof chrome` - gives pids of matching processes. simple and short.

## background process
- ran `sleep 300 &`
- job number `[1]` and actual pid are different
- `[1]` is bash's own number, pid is os's number
- did not go deep into jobs for now - will do later

## signals
- `kill` command sends signal to a process
- SIGTERM = -15 = graceful (process gets time to cleanup)
- SIGKILL = -9 = forceful (kills immediately, no cleanup chance)
- try SIGTERM first, only use -9 if that does not work
- -9 should not be first choice
