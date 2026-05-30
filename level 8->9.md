# Bandit Level 8 → 9

## Challenge
Password stored in `data.txt` — the only line that occurs exactly once.

## Commands Used
```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
sort data.txt | uniq -u
```

## What I Learned — sort and uniq in depth

### sort
- `sort filename` — sorts lines alphabetically
- `sort -r` — reverse order
- `sort -n` — sort numerically
- `sort -u` — sort and remove duplicates
- `sort -k` — sort by specific column/field

### uniq
- `uniq` — removes consecutive duplicate lines
- `uniq -u` — show only lines that appear exactly once
- `uniq -d` — show only duplicate lines
- `uniq -c` — count occurrences of each line

### Why sort Before uniq
`uniq` only works on consecutive duplicates.
`sort` first groups identical lines together so `uniq` can detect them properly.
Without sort, uniq misses non-consecutive duplicates.

### Why This Matters in Security
- Analyzing log files to find unique events
- Finding anomalies in large datasets
- Filtering repeated noise from command output
