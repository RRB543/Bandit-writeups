# Bandit Level 6 → 7

## Challenge
Password stored somewhere on the entire server with these properties:
- Owned by user bandit7
- Owned by group bandit6
- 33 bytes in size

## Commands Used
```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
```

## What I Learned

### The Problem Without 2>/dev/null
Searching from `/` gives hundreds of "Permission denied" errors
flooding the terminal and hiding the actual result.

### Standard Streams
- `stdin (0)` — input to a command
- `stdout (1)` — normal output
- `stderr (2)` — error messages

### Redirection
- `>` — redirect stdout to a file
- `2>` — redirect stderr specifically
- `/dev/null` — Linux trash bin, anything sent here disappears
- `2>/dev/null` — throw all errors away, show only real output
- `2>&1` — merge stderr into stdout
- `>>` — append to file instead of overwriting

### Why This Matters in Security
In pentesting and CTFs, commands often generate massive error noise.
`2>/dev/null` is used constantly to filter clean, useful output.
