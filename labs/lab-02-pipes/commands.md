# Commands — Lab 02 Pipes & Redirection

## Sample data
```bash
echo -e "apple\nbanana\napple\ncherry\nbanana\napple" > fruits.txt
echo -e "error: file not found\ninfo: starting\nwarning: low disk\nerror: timeout\ninfo: done" > app.log
```

## Pipes
```bash
cat fruits.txt | sort
cat fruits.txt | sort | uniq -c
cat fruits.txt | wc -l
cat app.log | grep "error"
cat app.log | grep -v "error"
```

## Redirection
```bash
echo "new line" > output.txt
echo "another line" >> output.txt
ls -la /nonexistent 2> errors.txt
ls -la /nonexistent 2>> errors.txt
```

## Chaining
```bash
mkdir testdir && cd testdir && touch file.txt && echo "chain worked"
ls /nonexistent || echo "fallback ran"
```

## Exit status
```bash
echo "check $?"
```
