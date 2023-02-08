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
## **0. Create and setup your Git and GitHub account**
> **Repo:**
> * GitHub repository: `holbertonschool-zero_day`
> * File: `README.md`


## **1. Repo-session**
Create a new directory called `git` in your repo.
Make sure you include a not empty `README.md` in your directory:
* at the root of your repository
* AND in the directory `git`
And important part: **Make sure your commit and push your code to Github - otherwise the Checker will always fail.**
> **Repo:**
> * GitHub repository: `holbertonschool-zero_day`

## **2. Coding fury road**
For the moment we have an empty project directory containing only a `README.md`. It’s time to code!

* Create these directories at the root of your project: `bash`, `c`, `js`
* Create these empty files:
    * `c/c_is_fun.c`
    * `js/main.js`
    * `js/index.js`
* Create a file `bash/best` with these two lines inside: `#!/bin/bash` and `echo "Best"`
* Create a file `bash/school` with these two lines inside: `#!/bin/bash` and `echo "School"`
* Add all these new files to git
* Commit your changes (message: “Starting to code today, so cool”) and push to the remote server
> **Repo:**
> * GitHub repository: `holbertonschool-zero_day`
> * Directory: git
> * File: `bash/best, bash/school, c/c_is_fun.c, js/main.js, js/index.js`

## **3. Collaboration is the base of a company**
A branch is like a copy of your project. It’s used mainly for:

* adding a feature in development
* collaborating on the same project with other developers
* not breaking your entire repository
* not upsetting your co-workers

The purpose of a branch is to isolate your work from the main code base of your project and/or from your co-workers’ work.

For this project, create a branch `update_script` and in this branch:

* Create an empty file named `bash/98`
* Update `bash/best` by replacing `echo "Best"` with `echo "Best School"`
* Update `bash/school` by replacing `echo "School"` with `echo "The school is open!"`
* Add and commit these changes (message: “My personal work”)
* Push this new branch [Tips](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository)

Perfect! You did an amazing update in your project and it’s isolated correctly from the main branch.

Ho wait, your manager needs a quick fix in your project and it needs to be deployed now:

* Change branch to `main`
* Update the file `bash/best` by replacing `echo "Best"` with `echo "This School is so cool!"`
* Delete the directory `js`
* Commit your changes (message: “Hot fix”) and push to the origin

Ouf, hot fix is done!
> **Repo:**
> * GitHub repository: `holbertonschool-zero_day`
> * Directory: git
> * File: `bash/best, bash/school, bash/98`

## **4. Collaboration: be up to date**
Of course, you can also work on the same branch as your co-workers and it’s best if you keep up to date with their changes.

For this task **– and only for this task –** please update your file `README.md` in the main branch from GitHub.com. It’s the **only time** you are allowed to update and commit from GitHub interface.

After you have done that, in your terminal:

* Get all changes of the main branch locally (i.e. your `README.md` file will be updated)
* Create a new file `up_to_date` at the root of your directory and in it, write the git command line used
* Add `up_to_date` to git, commit (message: “How to be up to date in git”), and push to the origin
> **Repo:**
> * GitHub repository: `holbertonschool-zero_day`
> * Directory: git
> * File: `README.md, up_to_date`

## **5. HAAA what did you do???**
Collaboration is cool, but not really when you update the same file at the same time…

To illustrate that, please merge the branch `update_script` to `main`: “Cool, all my changes will be now part of the main branch, ready to be deployed!”

**HHHHHHHAAAAAAAA**

```
CONFLICT (content): Merge conflict in bash/best
```
As you can see, you have conflicts between two branches on the same file.

Your goal now is to resolve conflicts by using the version of the branch `update_script`, and push the result to the origin.

At the end, you should have all your work from the branch `update_script` (new file and two updated files) and all latest `main` commits (new files, delete folder, etc.), without conflicts.
> **Repo:**
> * GitHub repository: `holbertonschool-zero_day`
> * Directory: git

## **6. Never push too much**
Create a `.gitignore` file and define a rule to never push ~ files (generated by Emacs). [Tips](https://git-scm.com/docs/gitignore)
> **Repo:**
> * GitHub repository: `holbertonschool-zero_day`
> * Directory: git
> * File: `.gitignore`


# **🧑‍💻Author**
## Javier Uc Ix [![GitHub](https://img.shields.io/badge/github-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/UCIX210)  [![twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/Zeroux0) [![Holberton](https://img.shields.io/badge/Holberton-E0143D?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADMAAAAzCAMAAAANf8AYAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAA5UExURUdwTP7+/vz8/P39/fDw8P7+/vv7+/7+/vr6+v7+/vf39/7+/v7+/v7+/v7+/vz8/P39/f39/f///+8FOYcAAAASdFJOUwCHQXUP+zbiK/EdmbjOqk5bZNUO1agAAAHASURBVEjHjZbbtoQgCEBTMTWz0v//2HNmsgTEGh5l7bhD0yQIzIdRyuTdT7+JjqncElazvAGLcoXLuj8RoOz59Zi19zrHcFJpTB3VhoP7KdenVfYQtuqLTfh1rYFJppYW+UYUFSqqQzyKnWrh0kRuBafroLpcRAhIhlklIVwKI/l8po37vd0q3R4NqaHhTFO3Kizh0UwLCIW0YcT+21cJMLMj9VzTbLln7lL1zCqY+QbjadF1l1RAZsIhTgdmIotwkztxxkwgtVGtlrNR+4D51qir8nzOXR4wCj/YTzDeXP3dJsITJpFwSnC2y2rH/Aekiix2HzBlodVBkqcRM9OWblbyNGS0zNDp7xjJtzBPj0x8RTjjhbxxhDNA6nMP0BMTeGNIo82YFfdbv0RFRvGdQ1bLuK8z78Af5gcst/zInJsnvrgm7AO6d/rphmPt9w4xBDxnKrkqn09bL+xRGF9OR05DHt4EfG7o1UTNfQwZw9oKUhkcM3KijHznwoiJfe1uaODcIblw3W0nItlaIzkch92zbPL/wefOOLbYqo3Njrb/93/nU92geZKTfvxLMq4ubtzXr/9vs0pivG/i4Un7B+SgTnORxWo/AAAAAElFTkSuQmCC)](https://holberton.anahuacmayab.mx/?utm_term=holberton&utm_campaign=Holberton%20-%20B%C3%BAsqueda%20-%20Inicial&utm_source=adwords&utm_medium=ppc&hsa_acc=1128264615&hsa_cam=15292939143&hsa_grp=136677203944&hsa_ad=562374335691&hsa_src=g&hsa_tgt=kwd-329582310924&hsa_kw=holberton&hsa_mt=b&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAiArY2fBhB9EiwAWqHK6jgmUH1beRZ4m69XomepNBorHj26GgPrYZy5t88Qg2DVKy0vXSLMuBoCphUQAvD_BwE)