# Bandit Level 7 → 8

## Challenge
Password stored in `data.txt` next to the word `millionth`.

## Commands Used
```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
grep "millionth" data.txt
```

## What I Learned — grep in depth

### Basic Usage
- `grep "pattern" filename` — search for pattern in file
- `grep -i` — case insensitive search
- `grep -n` — show line numbers
- `grep -v` — invert match, show lines that DON'T match
- `grep -r` — recursive search through directories
- `grep -c` — count matching lines
- `grep -l` — show only filenames that match
- `grep -w` — match whole word only
- `grep -A n` — show n lines after match
- `grep -B n` — show n lines before match

### Why grep Matters in Security
- Searching log files for specific IPs, errors, or events
- Finding passwords or sensitive data in files
- Filtering command output in CTFs and pentesting
- Combining with other commands using pipes `|`

### Pipe Concept
`command1 | command2` — output of command1 becomes input of command2
Example: `cat data.txt | grep "millionth"`
