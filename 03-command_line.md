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
pwd: show current working directory path
mkdir: create a directory
rm -d: delete a directory
touch: create a file with default permissions
rm: delete a file
mv *old name* *new name*: rename file
ls -a: list hidden files (ones that start with '.')
cp *source* *target*: copy file
man *command*: find out info about command
curl *url*: download data from url

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
ls: list directory contents
ls -a: list directory entries beginning with a dot
ls -l: list directory contents with more detailed information
ls -lh: list directory contents and use unit suffixes to reduce digits
ls -lah: list directory contents including ones beginning with a dot, and use unit suffixes 
ls -t: list directory contents, sorting by time modified (most recent first)
ls -Glp: list directory contents with more detailed information, colorized output, and slashes after directories

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> >
ls -1: display each entry on a line
ls -r: display files in reverse order
ls -d: displays only directories
ls -m: displays entries as a comma separated list
ls -x: displays entries in rows
---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > 
xargs can be used in tandem with another command in order to pass a constructed list of arguments to that command with a pipe. 
One example of how it can be used would be to create multiple folders in a directory by passing the names of them to mkdir with a pipe and xargs: 
echo 'one two three' | xargs mkdir

this will create 3 folders in the current directory, called one, two, and three.
 

