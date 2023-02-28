# Lab Report 3
## Helpful and Interesting Option Commands for `grep`:
### Option 1: `-c`
This command `grep -c <pattern> <filename(s)>` returns the number of times this pattern is found in the file(s).

Examples:\
In the current directory `written_2`, we want to find how many times "history" shows up in the file, `Vallarta-History.txt`,
so we enter the path to this file.
```
$ grep -c history travel_guides/berlitz2/Vallarta-History.txt
4
```

We can also use `-c` on the current directory by adding `ls|` in the front and it will search for the pattern in the name of files and subdirectories in the current directory. For example, the current directory `written_2` has two subdirectories, `non-fiction` and `travel_guides`.
```
$ ls| grep -c travel
1
```
Source: ChatGPT and https://swcarpentry.github.io/shell-novice/07-find/index.html

### Option 2: `-r`
This helpful command `grep -r <pattern> <directory>` recursively searches for the pattern in each file belonging in the directory and its subdirectories (if they exist) and outputs the line where the pattern was detected.

In the directory `written_2`
```
$ grep -r 
```
Source: ChatGPT and https://swcarpentry.github.io/shell-novice/07-find/index.html
### Option 3: `-l`
This command `grep -l <pattern> <filename(s)>` returns the file(s) that contain this pattern

In the directory `written_2`
```
$ grep -l
```
Source: ChatGPT and https://swcarpentry.github.io/shell-novice/07-find/index.html
### Option 4: `-v`
This interesting command `grep -v <pattern> <filename(s)>` inverts the search, in other words outputs the lines where the pattern was NOT detected.

Examples:\
In the directory `written_2`
```
$ grep -v 
```
Source: ChatGPT and https://swcarpentry.github.io/shell-novice/07-find/index.html
