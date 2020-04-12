# Lab 1: Hello, World!

In this lab, we will introduce ourselves and go over the structure of all CS KickStart
labs going forward. You will then learn about Linux, shells, and programming languages,
and you'll even get to write and run your first program!

#### Goals

* Cover lab structure  
* Setup programming environment  
* Run your first program  

## Lab Structure

CS KickStart labs are not graded. These labs are designed to teach and encourage critical
thinking rather than present direct content. If you have question, ask the instructor, officers,
or another participant at any time. Groupwork is always permitted, just remember to stop
your conversations when the instructor is presenting.

## Programming Environment

### Operating System

An operating system is the core of the computer. It's what makes it possible for you to interact
with your computer and the hardware. We're using the Linux operating system because it has features
that make it useful for programmers. Linux focuses more on giving you access to the nitty-gritty details
of controlling the computer, compared to some operating system's, like MacOS, that focus on making the
experience friendly for non-technical users. 

Linux is used in a lot of surpising places:

* Most machines that relay information across the internet  
* Over two-thirds of websites  
* All top 500 super computers  
* Many data centers  
* Even the entertainment systems on Delta Airlines!  

### Shell

A shell is an interface you can use to interact with the core of the computer. There are many kinds of shells.
One kind of shell is called a graphical user interface, or GUI. This is what you've been used to your whole life.
Another kind of shell is a command-line shell, or terminal. 

#### Activity: Working with Files on the Command Line.

Open up the terminal on your computer by searching for *terminal* among your computer's applications. You should
see a window that looks something like this (yours might be a different color):

![](images/terminal.png)

You can do things in your terminal by typing commands into the command line. Here are some common commands, many of
which we'll use in this lab:

| Command                   | Effect |
| ------------------------- | -------------------- |
| `pwd`                     | Print path of current working directory |
| `ls`                      | List directory content |
| `mkdir <directory>`       | Create new directory named <directory> |
| `cd <directory>`          | Change directory to <directory> |
| `cd ..`                   | Change directory to parent directory |
| `cd ~`                    | Change directory to root directory |
| `cp <file> <directory>`   | Copy <file> to <directory> |
| `mv <file-old> <file-new>`| Rename <file-old> to <file-new> |
| `mv <file> <directory>`   | Move <file> to <directory> |

*Note: directory is just another name for folder.*

Change directories to the root directory by typing the command `cd ~` into your terminal and pressing enter. Then type `ls` to see the contents of the root directory. You should see a directory named `Desktop`. Change to the Desktop directory by typing `cd Desktop`. Type `pwd` to see the path of your current working directory and confirm that you're in the right place.

Now type the following commands to create a new directory named `CS KickStart` (anything after the # symbol is a comment and won't be executed as part of the command):

```console
$ pwd                   # make sure that you're in the Desktop directory
$ ls                    # see the contents of the Desktop directory
$ mkdir cskickstart     # make a new directory called cskickstart
$ ls                    # see that cskickstart is now in the Desktop directory
$ cd cskiskstart        # change directory to the cskickstart directory
$ pwd                   # see that you're now in the Desktop/cskickstart directory
```

## Task 1 - Visual Debugger

For this task, use your visual debugger to run `stats_tests.cpp`, then

1. Step into the `test_sum_small_data_set()` function.
2. Step over until you reach the `sum` assertion.
3. Step into the `sum()` function in `stats.cpp` and view the content of the input vector.

![](images/image1.png)

Submit your visual debugger configuration.  Files locations are below, and relative to your
project 1 directory.  Note that the VS code file is a hidden file.

| Debugger      | Config file location |
| ------------- | -------------------- |
| Xcode         | `p1-stats.xcodeproj/project.pbxproj` |
| Visual Studio | `p1-stats.vcxproj` |
| VS Code       | `.vscode/launch.json` |

### Xcode

Xcode's `project.pbxproj` might not be visible in your finder window.  Here's how to open a finder window to the directory that contains a file.

```console
$ pwd
/Users/awdeorio/src/eecs280/p1-stats
$ open -R p1-stats.xcodeproj/project.pbxproj
```

### VS Code
VS Code's `.vscode/` directory is hidden.  You might need to make hidden files visible to locate it.

## Task 2 - Gitlab Commit Log

Next, you should open your Gitlab repository for project 1 and go into
the _Commits_ tab, where a list of all the uploaded commits should
appear. If you followed the setup guide completely and correctly, this
page should already show 3 commits, as you can see below.

![](images/image2.png)

View a text version of the same git log.
```console
$ git log
commit 4d375b45357b4b39822ad48c62c6988910258370 (HEAD -> master, origin/master)
Author: Andrew DeOrio <awdeorio@umich.edu>
Date:   Fri Jan 12 16:14:02 2018 -0500

    Added quick start to README

commit e016bfad5a6371097ea00380aedd3e22ee63f754
Author: Andrew DeOrio <awdeorio@umich.edu>
Date:   Fri Jan 12 16:07:36 2018 -0500

    Added README

commit a13e2521fab6488458c912f598d6d5f89d429484
Author: Andrew DeOrio <awdeorio@umich.edu>
Date:   Fri Jan 12 15:59:25 2018 -0500

    Initial commit.  Starter files with function stubs.
```

Save the text to a file called `gitlog.txt`.
```console
$ git log > gitlog.txt
```


## Task 3 - Compiling the Project Locally

Now, open a new terminal window and navigate to your project 1 folder.
There you should run the following list of commands, making sure that
the compilation is successful.

### Command List

```console
$ echo "Hello <your uniqname here>"
$ hostname
$ make clean
$ make stats_tests.exe
$ make stats_public_test.exe
$ make main.exe
```

This is how it should look, if you do it after finishing the setup
guide.

![](images/image4.png)

Copy everything in your terminal (both the commands and their output)  to a plain text file file called `localhost.txt`.


## Task 4 - Compiling on CAEN (through `ssh`)

Finally, copy your project over to CAEN and connect through `ssh`
again. There, you should run the same list of commands as Task 3,
making sure that the compilation is successful.

Also, run these additional commands.
```console
$ whoami
$ whoami | sha1sum
```

![](images/image3.png)

Copy everything in your terminal (both the commands and their output)  to a plain text file file called `caen.txt`.

## Submit

Submit all files to the autograder.
