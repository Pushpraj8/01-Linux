# Day 2 — Pipes, Redirection & Exit Status

### Pipes & Redirection

* `|` → The output of one command becomes the input of another command.
* `>` → Redirects output to a file and **overwrites** the existing content.
* `>>` → Redirects output to a file and **appends** to the existing content.
* `1>` → Redirects **stdout** (standard output); same as `>`.
* `2>` → Redirects **stderr** (error output) to a file and **overwrites** it.
* `2>>` → Redirects **stderr** to a file and **appends** to it.

### Exit Status

* `$?` → Displays the exit status of the **last executed command**.
* `0` = Success
* **Non-zero** = Failure
* `&&` → The next command runs **only if** the previous command succeeds.
* `||` → The next command runs **only if** the previous command fails.
* `echo` → Used to print a value or output.

### Intentionally Skipped for Now

* `2>&1`
* `tee`

### Why I Skipped These
didn't touch `2>&1` or `tee` today - figured i'll actually get why they matter once i'm writing scripts and need to combine outputs right now it would've just been memorizing syntax

Also pushing `awk`, `sort`, `uniq`, `tr`, `xargs`, `cut` to sunday so i wanted to give them proper time instead of rushing at the end of a long day

### Text-Processing Topics

The following topics will be covered in the **Sunday skipped-topics session**:

* `awk`
* `sort`
* `uniq`
* `tr`
* `xargs`
* `cut`

**Day 2 is complete, including the practical test.**
