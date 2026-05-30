# Bandit Level 2 → 3

## Challenge
Password stored in a file called `spaces in this filename` in the home directory.

## Commands Used
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
cat "spaces in this filename"
```

## What I Learned
- Linux treats spaces as separators between commands and arguments
- Wrapping filename in quotes tells Linux to treat it as one single filename
- Alternative method using backslash also works:
  cat spaces\ in\ this\ filename
- Tab autocomplete in terminal automatically adds the backslashes for you
