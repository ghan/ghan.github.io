---
layout: post
title: Bash Cheatsheet
---

Common Bash commands and a few handy tricks

## Basics
* Navigation
```bash
cd .. # go up one
cd ~ # go to home
pwd # current folder
ls # list files, -a hidden, -l more info, -R recursive
```

* File management
```bash
mv a.txt b.txt # rename to b.txt
mv a.txt ../other/folder/ # move
cp a.txt a-copy.txt # copy
mkdir new_directory # create new directory
touch file.py # create new file
rm oldfile.txt # remove file
rm -r full_folder/ # delete folder and its contents
```

## File Editor / Vim
```bash
i # invoke Insert mode for editing
o # append a new line after current line and invoke Insert mode
cc # clear current line and invoke Insert mode
u # undo
ESC # stop editing and return to Command mode
/search # searches for the regex pattern, in this case 'search'
n # next search result
:w # save
:wq # save and quit
:q # quit
:q! # quit without saving
```

## History 
```bash
cd - # go back a directory
history # view all commands
!! # last command
<Up key> # last command
```
Also, `<Ctrl-R>` then type to search history. `<Ctrl-R>` to cycle through results, `<Enter>` to execute.

## Process Management
```bash
command1 ; command2 # run command2 after command1
command1 && command2 # run command2 if command1 succeeds
command1 || command2 # run command2 if command1 fails
command1 & command2 # run at same time
ps -e # show all processes
command & # run in background
kill 1234 # kills process by pid
killall python # kill by name
kill -9 1234 # force kill
```

## Searching/finding
* Grep
    * can be used to filter a command by keyword eg `history` or `ps -e`
    * can also search contents of files:
    ```bash
    grep -r nav ./layouts/ # searches all items in layouts folder for 'nav'
    grep -lr nav . # lists names
    grep -ir Nav . # ignore case
    grep -er '(http|ftp)s?:' # regex
    ```
* Find
```bash
find . -name *.py # find all files in this dir with .py extension
find . -iname Bill.py # ignore case
find . -mtime 7 -iname readme # finds any file with 'readme' in the name modified in the last 7 days
```

## Misc Tricks
* Autocomplete 
    * <Tab> once to autocomplete a filename.
    * <Tab> twice to view all options
* Piping
```bash
history | grep python # runs history command but filtered on 'python'
```
* Variables
```bash
NAME="ghan"
echo "Hi $GHAN"
env # show all vars
```




