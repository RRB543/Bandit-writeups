# Bandit Level 0 → 1

## Challenge
Password stored in a file called `readme` in the home directory.

## Commands Used
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
cat readme
```

## What I Learned
- SSH is used to remotely connect to a Linux server
- Port 2220 means the server is not using the default SSH port (22)
- `cat` reads and prints the contents of a file
- Every Bandit level uses the found password to SSH into the next level
