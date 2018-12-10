# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  


pwd: show current working directory path
mkdir: create a directory
rmdir: remove a directory
touch: create a file (touch <filename>)
rm: remove a file
mv: rename a file (can rename and move it to a different directory)
ls: list files (not including hidden files)
la (or ls -a): list all files including hidden files
cp: copy a file (to another directory or to a new filename) 
sudo: activate root directory access

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

ls lists the files (and directories) in the directory
ls -a lists all the files and directories (including hidden files)
ls -l lists with long form information including file size and when it was created
ls -lh is the human readable version of ls -l
ls -lah in human readable, long form version of ls -a
ls -t is a sorted version of ls by filetype by time instead of alphabetically
ls -Glp is a long list form with no group names and adding a / after directories
 
---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

I don't really have favorites, but -r can be useful if you are looking for something in a directory

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

xargs allows you to give a command input from the keyboard instead of an arguement. Several commands require an arguement to run, so xargs is useful as it allows you to run the commands with input from the keyboard. Or input that is output from another file.
 

