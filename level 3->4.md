# Bandit Level 3 → 4

## Challenge
Password stored in a hidden file inside the `inhere` directory.

## Commands Used
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
cd inhere
ls -la
cat .hidden
```

## What I Learned
- Hidden files in Linux start with a `.` (dot)
- `ls` alone does not show hidden files
- `ls -la` shows all files including hidden ones
- `-l` gives detailed list, `-a` shows hidden files
- `cd` is used to navigate into a directory
