# Bandit Level 4 → 5

## Challenge
Password stored in the only human-readable file inside the `inhere` directory.
There are multiple files, only one contains readable text.

## Commands Used
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
cd inhere
file ./-*
cat ./-file07
```

## What I Learned
- `file` command tells you what type of content a file contains
- `file ./-*` checks all files at once using wildcard `*` — no need to check one by one
- Human-readable means ASCII text — the rest are binary/data files
- Only the ASCII text file contains the password
- Binary files display garbage characters if you try to `cat` them
