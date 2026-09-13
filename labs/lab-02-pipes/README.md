# Lab 02 — Pipes & Redirection

## What I did
Today I practiced pipes, redirection, and exit status created sample data (`fruits.txt`, `app.log`), then used `|` to chain commands — `sort`, `uniq -c`, `grep`, `wc -l`. Practiced `>` (overwrite) and `>>` (append), sent stderr to a file with `2>`, and tested `&&` and `||` for command chaining. Also checked exit status with `$?`.

## What went wrong
At first I ran the output capture command without creating the target folder, so it threw a "No such file or directory" error. Also, when I ran `ls /nonexistent` inside the `{ ... }` block, the error message went to the terminal instead of the file — because stderr isn't redirected by default with just `>`.

## How I fixed it
Created the `lab-02-pipes` folder first with `mkdir -p`, then re-ran the output capture. For the stderr issue, realized that `> file` only redirects stdout — stderr still goes to the terminal. To catch both, I'd need `2>&1` or `&>`, which I'll learn properly later.

## What I learned
- `|` sends one command's output as input to the next command
- `>` overwrites a file, `>>` appends to it
- `2>` redirects only stderr — stdout still goes to terminal
- `&&` runs the next command only if the previous succeeded
- `||` runs the next command only if the previous failed
- `$?` gives the exit code of the last command — `0` means success, anything else means failure (e.g. `ls /nonexistent` returned `2`)
