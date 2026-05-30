# Bandit Level 1 → 2

## Challenge
Password stored in a file called `-` in the home directory.

## Commands Used
```bash
cat ./-
```

## What I Learned
- Files named `-` are special in Linux — terminal treats `-` as stdin by default
- Use `./` prefix to tell Linux "this is a file in current directory, not a flag"
- This is called a "special character filename"
