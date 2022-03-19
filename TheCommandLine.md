# The Command Line

## What is The Command Line
The command line: is a text interface to the system. You are able to enter commands by typing them on the keyboard. You can do what ever you can do with GUI but with words (command lines).

let's talk about baths:
There are 2 types of paths we can use, absolute and relative. Whenever we refer to a file or directory we are using one of these paths.
1. Absolute paths specify a location (file or directory) in relation to the root directory.
2. Relative paths specify a location (file or directory) in relation to where we currently are in the system.

## Important Commands

- The first command we are going to learn is "pwd" which stands for Print Working Directory.It tells you what your current or present working directory is.

- In order to move around in the system we use a command called "cd" which stands for change directory.

- To know what is in this directory we can use "ls" it give us a List the contents of a directory.

1. If you run the command cd without any arguments then it will always take you back to your home directory.
2. you can put a path after cd to go there. if there is a space we can use '__ __'. because anything inside quotes is considered as a single item.

- We can use "-a" to show the hidden files.To make a file or directory hidden all you need to do is create the file or directory with it's name beginning with a . or rename it to be like that.

- To make a directory we can use "mkdir" which is short for Make Directory. and to delete one we can use "rmdir" with "-r" if it is not empty.

- To make a new file we can use "touch". and to delete a file we use "rm" wiche is short for remove.

- to copy we use "cp" then the path of the file/directory(with "-r") we want to copy then the path were we want to copy it. and we can use "mv" to move a file or a directory.

## Manual pages
The manual pages are a set of pages that explain every command available on your system including what they do, how you run them and what command line arguments they accept. we can bring the by use "man" command like this
> $man ls

That will give us this
>Name
>    ls - list directory contents
> 
> Synopsis
>     ls [option] ... [file] ...
> 
> Description
>    List information about the FILEs (the current directory by default). Sort > > entries alphabetically if none of -cftuvSUX nor --sort is specified.
>  
>    Mandatory arguments to long options are mandatory for short options too.
> 
>    -a, --all
>        do not ignore entries starting with .
> 
>    -A, --almost-all
>        do not list implied . and .. 

- To exit the manual pages press 'q' for quit.

- we can use "man -k <search something\>" to search inside a manual page and 'n' button for next result.

<br>

#### Here is the Refrence [Linux Tutorial](https://ryanstutorials.net/linuxtutorial/commandline.php)

#### And here is a CheatSheet [Linux Tutorial Cheat Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)