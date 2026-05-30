# Bandit Level 9 → 10

## Challenge
Password stored in `data.txt` — a human-readable string preceded by several `=` characters.
File contains mostly binary data.

## Commands Used
```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
strings data.txt | grep "==="
```

## What I Learned — strings, grep and piping

### strings command
- `strings filename` — extracts all human-readable text from any file
- Works on binary files — pulls out readable ASCII sequences
- Minimum 4 characters by default
- `strings -n 10` — only show strings of 10+ characters
- Used heavily in malware analysis and reverse engineering

### Pipeline Flow
data.txt → strings → grep "===" → password
- `strings data.txt` extracts readable text from binary file
- `|` passes that output to grep
- `grep "==="` filters only lines with === characters
- Final output is the password line

### Why Piping is Powerful
Instead of saving intermediate output to files,
pipes chain commands so output flows directly into the next command.
Each command does one thing well — combined they solve complex problems.

### Why This Matters in Security
- `strings` is used in malware analysis to extract readable content from binaries
- Finding hardcoded passwords, URLs, or keys inside executable files
- First tool analysts run on suspicious files
