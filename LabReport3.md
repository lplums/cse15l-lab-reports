# Lab Report 3
## Helpful and Interesting Options for `grep`:
### Option 1: `-c`
This command `grep -c <pattern> <filename>`

Examples:\
In the directory `Docsearch`
```
$ grep -c 
3
```

### Option 2: `-r`
This command `grep -r <pattenr> <directory>` recursively searches for the pattern in each file belonging in the directory and its subdirectories (if they exist) and outputs the line where the pattern was detected.

In the directory `Docsearch`
```
$ grep -r 
```
### Option 3: `-l`

### Option 4: `-v`
This interesting command `grep -v <pattern> <filename>` inverts the search, in other words outputs the lines where the pattern was NOT detected.
