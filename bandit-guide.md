# Over the Wire: Bandit
---
### [Level 0](https://overthewire.org/wargames/bandit/bandit0.html)
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
### [Level 0 -> Level 1](https://overthewire.org/wargames/bandit/bandit1.html)
```bash
cat readme
```
### [Level 1 -> level 2](https://overthewire.org/wargames/bandit/bandit2.html)
```
cat ./-
```
**Easter Egg**- Creating a dash file is not possible directly, one can use the following to create a dash file -
```bash
echo "random text" > -
```
### [Level 2 -> Level 3](https://overthewire.org/wargames/bandit/bandit3.html)
```bash
cat spaces\ in\ this\ filename
```
### [Level 3 -> Level 4](https://overthewire.org/wargames/bandit/bandit4.html)
```bash
cd inhere/ && cat ...Hiding-From-You
```
### [Level 4 -> Level 5](https://overthewire.org/wargames/bandit/bandit5.html)
```bash
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
```
### [Level 5 -> Level 6](https://overthewire.org/wargames/bandit/bandit6.html)
```bash
find ./ -maxdepth 3 -type f -size 1033c -exec ls -lh {} \;|tee /dev/tty | awk '{print$9}' | xargs file | tee /dev/tty | awk -F ':' '{print$1}' | xargs cat
```
**Note** - *tee* command duplicates output to file and screen. *pipe*(|) command passes the output to another command. *xargs* command build and execute commands form input
```bash
find . -name "*.txt" | tee file_list.txt | xargs cat
```
**Easter Egg** - using tee /dev/tty displays it on the terminal
### [Level 6 -> Level 7](https://overthewire.org/wargames/bandit/bandit7.html)
```bash
find / -user bandit7 -group bandit6 -size 33c 2> /dev/null | xargs cat
```
### [Level 7 -> Level 8](https://overthewire.org/wargames/bandit/bandit8.html)
```bash
grep "millionth" data.txt | awk '{print$2}'
```
### [Level 8 -> Level 9](https://overthewire.org/wargames/bandit/bandit9.html)
```bash
sort data.txt | uniq -u
```
### [Level 9 -> Level 10](https://overthewire.org/wargames/bandit/bandit10.html)
```bash
strings data.txt | grep === | tail -1 | awk '{print$2}'
```
### [Level 10 -> Level 11](https://overthewire.org/wargames/bandit/bandit11.html)
```bash
base64 -d data.txt | awk '{print$4}'
```

Save progress - dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
