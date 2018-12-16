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

> >
* pwd: show current working directory path
* mkdir: creating a directory
* rm -r: deleting a directory
* touch filename.txt: creating a file using `touch` command
* rm: deleting a file
* mv: renaming a file
* ls -a: listing hidden files
* cp sourcefile.txt destination/directory: copying a file from one directory to another
* sed 's/newword/wordtoreplace' file.txt: replaces words in given file
* cd: changes directory (also cd ..)

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

> > 
* ls     shows all file in working directory
* ls -a  shows all files including hidden files
* ls -l  lists all contents in long format
* ls -lh  lists files in long for with headers
* ls -lah  lists files in long form including hidden files
* ls -t  orders files and directory by last time modified
* ls -Glp   lists files in long form with a port specified


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 
* -d	Displays only directories.
* -m	Displays the names as a comma-separated list.
* -u	Displays files by the file access time.
* -x Displays files as rows across the screen.
* -1	Displays each entry on a line.

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > 
'xargs' is a command used to build execution pipeline fmor standard input. For example, (from https://shapeshed.com/unix-xargs/) in "find /tmp -mtime +14 | xargs rm" files older than 2 weeks are piped into xargs and then the remove command is run on the files.

 

