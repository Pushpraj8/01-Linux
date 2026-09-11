Day 2 done
today was pipes and redirection | takes one command's output and feeds it into another > overwrites a file with output >> appends instead and stdout/stderr are actually separate things - 1> and 2> let you split them, which i didn't know before today lol
exit status was the other half $? gives you 0 for success anything else means it failed && runs the next command only if the first one worked, || only if it didn't simple but useful for chaining stuff.
didn't touch 2>&1 or tee today, figured i'll actually get why they matter once i'm writing scripts and need to combine outputs, right now it would've just been memorizing syntax
also pushing awk, sort, uniq, tr, xargs, cut to sunday wanted to give them proper time instead of rushing at the end of a long day
test done moving to day 3 tomorrow
