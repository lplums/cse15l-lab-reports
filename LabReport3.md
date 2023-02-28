# Lab Report 3
## Helpful and Interesting Option Commands for `grep`:
### Option 1: `-c`
This command `grep -c <pattern> <filename(s)>`

Examples:\
In the directory `Docsearch`
```
$ grep -c 
3
```

### Option 2: `-r`
This helpful command `grep -r <pattern> <directory>` recursively searches for the pattern in each file belonging in the directory and its subdirectories (if they exist) and outputs the line where the pattern was detected.

In the directory `Docsearch`
```
$ grep -r 
```
### Option 3: `-l`
This command `grep -l <pattern> <filename(s)>` returns the file(s) that contain this pattern

In the directory `Docsearch`
```
$ grep -l
```

### Option 4: `-v`
This interesting command `grep -v <pattern> <filename(s)>` inverts the search, in other words outputs the lines where the pattern was NOT detected.

Examples:\
In the directoru
