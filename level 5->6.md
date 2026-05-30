# Bandit Level 5 → 6

## Challenge
Password stored somewhere under `inhere` directory with these properties:
- Human-readable
- 1033 bytes in size
- Not executable

## Commands Used
```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
cd inhere
find . -type f -size 1033c ! -executable
cat ./maybehere07/.file2
```

## What I Learned — find command in depth

### Conditions/Tests
- `-type f` — files only, `-type d` — directories only
- `-size 1033c` — exactly 1033 bytes (`c`=bytes, `k`=KB, `M`=MB)
- `-name` / `-iname` — search by name (iname is case insensitive)
- `-user` / `-group` — filter by owner or group
- `! -executable` — NOT operator, exclude executable files
- `-readable` / `-writable` — filter by permission type
- `-empty` — find empty files or directories
- `-mtime` / `-newer` — filter by modification time

### Actions
- `-print` — default, prints matching file paths
- `-delete` — deletes matching files
- `-exec command {} \;` — runs command on each result one by one
- `-exec command {} +` — runs command on all results at once (faster)
- `-ok` — like exec but asks confirmation before each action
- `-ls` — detailed listing like `ls -l`
- `-printf` — custom formatted output

## Key Insight
`find` is one of the most powerful Linux commands for forensics and pentesting
— locating files by properties rather than names is a real investigative skill.
