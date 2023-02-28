# Lab Report 3
## Helpful and Interesting Option Commands for `grep`:
### Option 1: `-c`
This command `grep -c <pattern> <filename(s)>` returns the number of times this pattern is found in the file(s).

Examples:

In the current directory `written_2`, we want to find how many times "history" shows up in the file, `Vallarta-History.txt`,
so we enter the path to this file.
```
$ grep -c history travel_guides/berlitz2/Vallarta-History.txt
4
```

We can also use `-c` on the current directory by adding `ls|` in the front. It will search for the pattern in the name of the files and subdirectories in the current directory. For example, this current directory `written_2` holds two subdirectories, `non-fiction` and `travel_guides`.
```
$ ls| grep -c travel
1
```
Source: ChatGPT and https://swcarpentry.github.io/shell-novice/07-find/index.html

### Option 2: `-r`
This helpful command `grep -r <pattern> <directory>` recursively searches for the pattern in each file belonging in the directory and its subdirectories (if they exist) and outputs the line where the pattern was detected.

Examples:

Suppose we want to find the word "Lucayans" in all these files contained in the current directory,`written_2`. Then this command will return the filename and the line where the word "Lucayans" was found.
```
$ grep -r Lucayans
travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
We can also combine this command with the previous command,`-c`, to find the amount of times a pattern is found in all these files of the directory. It will return each file with their count.
```
$ grep -rc the non-fiction/OUP/Abernathy
non-fiction/OUP/Abernathy/ch1.txt:68
non-fiction/OUP/Abernathy/ch14.txt:57
non-fiction/OUP/Abernathy/ch15.txt:62
non-fiction/OUP/Abernathy/ch2.txt:63
non-fiction/OUP/Abernathy/ch3.txt:50
non-fiction/OUP/Abernathy/ch6.txt:60
non-fiction/OUP/Abernathy/ch7.txt:56
non-fiction/OUP/Abernathy/ch8.txt:67
non-fiction/OUP/Abernathy/ch9.txt:41
```

Source: ChatGPT and https://swcarpentry.github.io/shell-novice/07-find/index.html
### Option 3: `-l`
This command `grep -l <pattern> <filename(s)>` returns the file(s) that contain this pattern.

Examples:

We can put enter multiple files and this command will return which files contain this specified pattern.
```
$ grep -l Vallarta travel_guides/berlitz2/Vallarta-History.txt travel_guides/berlitz2/Cuba-History.txt
travel_guides/berlitz2/Vallarta-History.txt
```
In this current directory, `written_2`, we can use the command `r` to recursively find the file that contains this pattern, "Lucayans" without naming all the files (very useful!).
```
$ grep -rl Lucayans
travel_guides/berlitz2/Bahamas-History.txt
```
Source: ChatGPT and https://swcarpentry.github.io/shell-novice/07-find/index.html
### Option 4: `-v`
This interesting command `grep -v <pattern> <filename(s)>` inverts the search, in other words outputs the lines where the pattern was **NOT** detected.

Examples:

Suppose we want the lines in the file `Nepal-History.txt` that **do not** contain the word "the" and we are in the current directory `written_2`.
```
$ grep -v the travel_guides/berlitz2/Nepal-History.txt




A Brief HistorY
Unity and Fragmentation
Unification
Modern Times
Religions of Nepal
Hinduism
Buddhism



```
We can also combine commands such as `l` with `-v` to find the files that do not contain the pattern.
```
$ grep -l Vallarta travel_guides/berlitz2/Vallarta-History.txt travel_guides/berlitz2/Cuba-History.txt
travel_guides/berlitz2/Cuba-History.txt
```
Source: ChatGPT and https://swcarpentry.github.io/shell-novice/07-find/index.html
