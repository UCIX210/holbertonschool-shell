![image](../img/basics.jpeg)
# **Basics**
Release date February 6, 2023
</p>

# **Table of Contents**
* [Resources](#Resources)
* [Learning Objectives](#Learning-Objectives)
* [Requirements](#Requirements)
* [Tasks](#Tasks)
    * 0-Where am I?
    * 1-What’s in there?
    * 2-There is no place like home
    * 3-The long format
    * 4-Hidden files
    * 5-I love numbers
    * 6-Welcome
    * 7-Betty in my first directory
    * 8-Bye bye Betty
    * 9-Bye bye My first directory
    * 10-Back to the future
    * 11-Lists
    * 12-File type
    * 13-We are symbols, and inhabit symbols
    * 14-Copy HTML files
    * 15-Let’s move
    * 16-Clean Emacs
    * 17-Tree
* [Author](#author)

# **🔗Resources**
 * [What Is “The Shell”?](http://linuxcommand.org/lc3_lts0010.php)
 * [Navigation](http://linuxcommand.org/lc3_lts0020.php)
 * [Looking Around](http://linuxcommand.org/lc3_lts0030.php)
 * [A Guided Tour](http://linuxcommand.org/lc3_lts0040.php)
 * [Manipulating Files](http://linuxcommand.org/lc3_lts0050.php)
 * [Working With Commands](http://linuxcommand.org/lc3_lts0060.php)
 * [Reading Man pages](http://linuxcommand.org/lc3_man_pages/man1.html)
 * [Keyboard shortcuts for Bash](https://www.howtogeek.com/181/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/)
 * [LTS](https://wiki.ubuntu.com/LTS)
 * [Shebang](https://en.wikipedia.org/wiki/Shebang_%28Unix%29)

 # **🧠Learning Objectives**
 ## General
 * What does RTFM mean?
 * What is a Shebang
 ## What is the Shell
 * What is the shell
 * What is the difference between a terminal and a shell
 * What is the shell prompt
 * How to use the history (the basics)
 ## Navigation
 * What do the commands or built-ins `cd`, `pwd`, `ls` do
 * How to navigate the filesystem
 * What are the . and .. directories
 * What is the working directory, how to print it and how to change it
 * What is the root directory
 * What is the home directory, and how to go there
 * What is the difference between the root directory and the home directory of the user root
 * What are the characteristics of hidden files and how to list them
 * What does the command `cd` - do
 ## Looking Around
 * What do the commands `ls`, `less`, `file` do
 * How do you use options and arguments with commands
Understand the ls long format and how to display it
 * A Guided Tour
 * What does the `ln` command do
 * What do you find in the most common/important directories
 * What is a symbolic link
 * What is a hard link
 * What is the difference between a hard link and a symbolic link
 ## Manipulating Files
 * What do the commands cp, mv, rm, mkdir do
 * What are wildcards and how do they work
 * How to use wildcards
 ## Working with Commands
 * What do `type`, `which`, `help`, `man` commands do
 * What are the different kinds of commands
 * What is an alias
 * When do you use the command help instead of man
 ## Reading Man Pages
 * How to read a man page
 * What are man page sections
 * What are the section numbers for User commands, System calls and Library functions
 ## Keyboard Shortcuts for Bash
 * Common shortcuts for Bash
 ## LTS
 * What does `LTS` mean?

# **🛠Requirements**
 * Allowed editors: `vi`, `vim`, `emacs`
 * All your scripts will be tested on Ubuntu 20.04 LTS
 * All your scripts should be exactly two lines long (`$ wc -l file` should print 2)
 * All your files should end with a new line ([why?](https://unix.stackexchange.com/questions/18743/whats-the-point-in-adding-a-new-line-to-the-end-of-a-file/18789))
 * The first line of all your files should be exactly `#!/bin/bash`
 * A `README.md` file at the root of the repo, containing a description of the repository
 * A `README.md` file, at the root of the folder of this project, describing what each script is doing
 * You are not allowed to use backticks, `&&`, `||` or `;`
 * All your scripts must be executable. To make your file executable, use the `chmod` command: `chmod u+x file`. Later, we’ll learn more about how to utilize this command.

# **🚧Tasks**
## **0. Where am I?**
Write a script that prints the absolute path name of the current working directory.
Example:
```
$ ./0-current_working_directory
/0x00-shell_basics
$
```
> **Repo:**
> * GitHub repository: `holbertonschool-shell`
> * Directory: basics
> * File: [0-current_working_directory]()


## **1. What’s in there?**
Display the contents list of your current directory.

Example:
```
$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop Downloads   Library Music Public
$
```
> **Repo:**
> * GitHub repository: `holbertonschool-shell`
> * Directory: basics
> * File: [1-listit]()

## **2. There is no place like home**
Write a script that changes the working directory to the user’s home directory.

 * You are not allowed to use any shell variables
```
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ echo $HOME
/home/julien
julien@ubuntu:/tmp$ source ./2-bring_me_home
julien@ubuntu:~$ pwd
/home/julien
julien@ubuntu:~$ 
```
> **Repo:**
> * GitHub repository: `holbertonschool-shell`
> * Directory: basics
> * File: [2-bring_me_home]()

## **3. The long format**
Display current directory contents in a long format

Example:
```
$ ./3-listfiles
total 32
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
$
```
> **Repo:**
> * GitHub repository: `holbertonschool-shell`
> * Directory: basics
> * File: [3-listfiles]()

## 4. Hidden files
Display current directory contents, including hidden files (starting with `.`). Use the long format.

Example:
```
$ ./4-listmorefiles
total 32
drwxr-xr-x@ 6 sylvain staff 204 Jan 25 00:29 .
drwxr-xr-x@ 43 sylvain staff 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:41 4-listmorefiles
$
```
> **Repo:**
> * GitHub repository: `holbertonschool-shell`
> * Directory: basics
> * File: [4-listmorefiles]()

## 5. I love numbers
Display current directory contents.

 * Long format
 * with user and group IDs displayed numerically
 * And hidden files (starting with .)
Example:
```
$ ./5-listfilesdigitonly
total 32
drwxr-xr-x@ 6 501 20 204 Jan 25 00:29 .
drwxr-xr-x@ 43 501 20 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:23 1-listfiles
-rwxr-xr-x@ 1 501 20 19 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 501 20 20 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:41 4-listmorefiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:43 5-listfilesdigitonly
$
```
> **Repo:**
> * GitHub repository: `holbertonschool-shell`
> * Directory: basics
> * File: [5-listfilesdigitonly]()

## 6. Welcome
Create a script that creates a directory named `my_first_directory` in the `/tmp/` directory.

Example:
```
$ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
$
```
> **Repo:**
> * GitHub repository: `holbertonschool-shell`
> * Directory: basics
> * File: [6-firstdirectory]()

## 7. Betty in my first directory
Move the file `betty` from `/tmp/` to `/tmp/my_first_directory`.

Example:
```
$ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
$
```
> **Repo:**
> * GitHub repository: `holbertonschool-shell`
> * Directory: basics
> * File: [5-listfilesdigitonly]()


# **🧑‍💻Author**
## Javier Uc Ix [![GitHub](https://img.shields.io/badge/github-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/UCIX210)  [![twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/Zeroux0) [![Holberton](https://img.shields.io/badge/Holberton-E0143D?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADMAAAAzCAMAAAANf8AYAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAA5UExURUdwTP7+/vz8/P39/fDw8P7+/vv7+/7+/vr6+v7+/vf39/7+/v7+/v7+/v7+/vz8/P39/f39/f///+8FOYcAAAASdFJOUwCHQXUP+zbiK/EdmbjOqk5bZNUO1agAAAHASURBVEjHjZbbtoQgCEBTMTWz0v//2HNmsgTEGh5l7bhD0yQIzIdRyuTdT7+JjqncElazvAGLcoXLuj8RoOz59Zi19zrHcFJpTB3VhoP7KdenVfYQtuqLTfh1rYFJppYW+UYUFSqqQzyKnWrh0kRuBafroLpcRAhIhlklIVwKI/l8po37vd0q3R4NqaHhTFO3Kizh0UwLCIW0YcT+21cJMLMj9VzTbLln7lL1zCqY+QbjadF1l1RAZsIhTgdmIotwkztxxkwgtVGtlrNR+4D51qir8nzOXR4wCj/YTzDeXP3dJsITJpFwSnC2y2rH/Aekiix2HzBlodVBkqcRM9OWblbyNGS0zNDp7xjJtzBPj0x8RTjjhbxxhDNA6nMP0BMTeGNIo82YFfdbv0RFRvGdQ1bLuK8z78Af5gcst/zInJsnvrgm7AO6d/rphmPt9w4xBDxnKrkqn09bL+xRGF9OR05DHt4EfG7o1UTNfQwZw9oKUhkcM3KijHznwoiJfe1uaODcIblw3W0nItlaIzkch92zbPL/wefOOLbYqo3Njrb/93/nU92geZKTfvxLMq4ubtzXr/9vs0pivG/i4Un7B+SgTnORxWo/AAAAAElFTkSuQmCC)](https://holberton.anahuacmayab.mx/?utm_term=holberton&utm_campaign=Holberton%20-%20B%C3%BAsqueda%20-%20Inicial&utm_source=adwords&utm_medium=ppc&hsa_acc=1128264615&hsa_cam=15292939143&hsa_grp=136677203944&hsa_ad=562374335691&hsa_src=g&hsa_tgt=kwd-329582310924&hsa_kw=holberton&hsa_mt=b&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAiArY2fBhB9EiwAWqHK6jgmUH1beRZ4m69XomepNBorHj26GgPrYZy5t88Qg2DVKy0vXSLMuBoCphUQAvD_BwE)