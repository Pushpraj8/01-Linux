# Commands — Lab 01 Filesystem

## Working directory setup
```bash
mkdir -p ~/lab-practice
cd ~/lab-practice
```

## Nested folders
```bash
mkdir -p projects/dev
mkdir -p projects/test
```

## Files create
```bash
touch projects/dev/main.py
touch projects/dev/notes.txt
touch projects/test/test.py
```

## Verify
```bash
pwd
ls -la
ls -la projects/
ls -la projects/dev/
ls -R
```

## Copy
```bash
cp projects/dev/main.py projects/test/
cp -r projects/dev projects/backup
```

## Move/Rename
```bash
mv projects/test/test.py projects/test/test_old.py
```

## Globbing
```bash
touch projects/dev/log1.log projects/dev/log2.log projects/dev/error.log
ls projects/dev/*.log
```

## Safe deletion
```bash
pwd
ls -la
rm -rf projects/backup
```

## Final check
```bash
ls -R
```
