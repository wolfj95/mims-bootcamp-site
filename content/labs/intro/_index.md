---
title: 0. Introduction
type: labs
---

# Getting started
Welcome to the MIMS Python Bootcamp 2021! We're glad you're here! 😄

This lab will introduce you to the programming environment we'll use for the bootcamp,
Jupyter Notebooks, and show you how to run your first Python program.

{{< hint warning >}}
If you haven't already finished setting up your computer, head over to the [setup page]({{< relref "setup" >}})
and complete the setup before you continue.
{{< /hint >}}

## Using the Terminal
Even though we will be using Jupyter Notebooks as the primary coding evnironment for this course,
we first need to figure out how to use Jupyter to access our code files. We will do this using a tool
called a terminal. 

{{< aside >}}
For computers running macOS, you will use an application called Terminal.

For computers running Windows, you will use an application called Windows Terminal.

These two terminals work pretty differently. However, they are similar enough that
we can use them the same way for the purposes of this course. For this section, we'll
show Mac and Windows content separately, but after that we can (mostly) use the same
instructions.
{{< /aside >}}

### Terminal: a new user interface


You're probably used to interacting with the files in your computer through a *Graphical User Interface
(GUI)* like Finder. Terminal allows us to interact with the files in our computer through a *Text-based
User Interface (TUI)*. The files in our computers are organized in nested folders known as
*directories*.

Let's use this interface to create a place to put the files we'll use for the course.

{{< code-action >}} Open a new Terminal window.

Terminal opens in your `home` directory for your user. You can tell this by looking at the
text before the `$`, called the prompt. Your prompt might look slightly different (for example,
it may include a username), but that's ok. 
{{< tabs "0" >}}
{{< tab "macOS" >}}
`~` is the symbol for the `home` directory.
```shell
Last login: Thu Aug 15 13:57:41 on ttys008
~$
```
{{< /tab >}}
{{< tab "Windows" >}}
```shell
PS C:\Users\jwolf> 
```
{{< /tab >}}
{{< /tabs >}}

{{< aside >}}
Sometimes you'll see {{< code-action >}} in a lab. This means that you
need do something that involves writing code or using your computer. You can use these as 
indicators for action items during labs.
{{< /aside >}}

#### What's in your home directory?

Anytime you see the prompt in your terminal, it means that it's ready to accept a command.
You can use commands to tell your terminal to do various things, like navigate your file
system or open files.

To see the files and subdirectories in the current directory, you can use the list command.
{{< code-action >}} Type `ls` into the command line (after the prompt) and press `return`.
This will list everything in the current directory.

{{< tabs "1" >}}
{{< tab "macOS" >}}
```shell
~$ ls
Applications  Desktop  Documents  Downloads	 Library  Movies  Music	 Pictures
```
{{< /tab >}}
{{< tab "Windows" >}}
For Windows, using the `ls -n` command can make the output more readable.
```shell
PS C:\Users\jwolf> ls -n
.ipython
Contacts
Desktop
Documents
Downloads
Favorites
```
{{< /tab >}}
{{< /tabs >}}

Here, you should see that `Desktop` is one of the subdirectories listed. Let's move into that
subdirectory.

{{< code-action >}} Type `cd Desktop` into the command line and press
`return` ("cd" stands for "change directory"). Notice how the path before the prompt changed
to tell us we're now on the Desktop.


{{< code-action >}} Then, list all the items in your `Desktop` directory using `ls`.

{{< tabs "2" >}}
{{< tab "macOS" >}}
```shell
~$ cd Desktop
~/Desktop$ ls
Screen Shot 2019-08-15 at 12.34.48 AM.png  dobby.gif			  warsaw-boarding-pass.pdf
lentil loaf gravy.pdf
```
{{< /tab >}}
{{< tab "Windows" >}}
```shell
PS C:\Users\jwolf> cd Desktop
PS C:\Users\jwolf\Desktop> ls -n
Bicycle
Cara
Fall
Numbers
bouquet1.png
bouquet2.png
Dropbox.lnk
```

{{< /tab >}}
{{< /tabs >}}

#### TUI vs. GUI

Compare what you see on your Desktop with the output of the 
command above. All of the files and folders are the same!
The Terminal really does show us the same files and directories as our GUI!

### Making the `mims_bootcamp` directory
We reccomend that you create the directory for your work in the course on your Desktop
(however, you can do it anywhere by navigating around your filesystem).

To create a new directory in your current location with the name `mims_bootcamp`,
run the following command:
{{< tabs "3" >}}
{{< tab "macOS" >}}
```shell
~/Desktop$ mkdir mims_bootcamp
```
{{< /tab >}}
{{< tab "Windows" >}}
```shell
PS C:\Users\jwolf\Desktop> mkdir mims_bootcamp
```
{{< /tab >}}
{{< /tabs >}}

{{< code-action >}} Now you can `cd` inside and get started!

{{< aside >}}
When copying commands from this website, be careful not to copy the prompt (`$`).
Only copy the commands and parameters that follow it.
{{< /aside >}}

## Intro Lab
Now that you can navigate in the Terminal, let's write some code! Throughout the course, we
will be using the Python programming language to help us perform computational tasks. In
this unit, we'll be using a software library called turtle to draw things with code. There
are many ways you can write and run Python programs. For this course, we will use
Jupyter Notebooks which allow us to write and run Python program all in one place.

The first lab will cover how to use Juptyer, how to draw with Python turtle, and how
to incorporate variables into your programs.

{{< code-action >}} Once you are in your `mims-bootcamp` directory, you can download the notebook for
this lab using the following command:

{{< tabs "4" >}}
{{< tab "macOS" >}}
```shell
~/Desktop/mims_bootcamp$ git clone https://github.com/wolfj95/mims-intro.git
```
{{< /tab >}}
{{< tab "Windows" >}}
```shell
PS C:\Users\jwolf\Desktop\mims_bootcamp> git clone https://github.com/wolfj95/mims-intro.git
```
{{< /tab >}}
{{< /tabs >}}

Now, you can use Jupyter to open the lab you just downloaded.

{{< code-action >}} Start by running Jupyter in your terminal:

{{< tabs "5" >}}
{{< tab "macOS" >}}
```shell
~/Desktop/mims_bootcamp$ jupyter notebook
```
{{< /tab >}}
{{< tab "Windows" >}}
```shell
python3 -m notebook
```
{{< /tab >}}
{{< /tabs >}}

Use the window that opened in your web browser to navigate to the `mims_intro` folder.
Then, click on the the `intro.ipynb` file to open it.

{{< code-action >}} Complete the lab in the Jupyter notebook.

## Wrapping up
{{< code-action >}} Once you have completed the lab or in the last 15 minutes of class, complete
[the check-in quiz for this lab](https://forms.gle/ghZED4EziHAhNQwd8).

Remember that you should complete the check-in
quiz individually.

{{< hint info >}}
You can check [the solutions to the quiz on Github](https://github.com/wolfj95/mims-intro/blob/main/quiz.ipynb).
{{< /hint >}}

---

## Resources

### Terminal commands
Here's a summary of the commands you just learned:
{{< tabs "6" >}}
{{< tab "macOS" >}}
| Command                 | Description |
| :---------------------- | :-----------|
| `cd Desktop/mims_bootcamp`| to change to the directory "mims_bootcamp" |
| `jupyter notebook`        | to open the Jupyter server and browser.   |
| `mkdir [name]`            | to create a new directory in the current location. |
{{< /tab >}}
{{< tab "Windows" >}}
| Command                 | Description |
| :---------------------- | :-----------|
| `cd Desktop/mims_bootcamp`| to change to the directory "mims_bootcamp" |
| `python3 -m notebook`        | to open the Jupyter server and browser.   |
| `mkdir [name]`            | to create a new directory in the current location. |
{{< /tab >}}
{{< /tabs >}}


### Common turtle commands
| Function |       Input      |   Example Use  | Explanation                                                                                                                      |
|:--------:|:----------------:|:--------------:|----------------------------------------------------------------------------------------------------------------------------------|
|  forward |      amount      |  forward(100)  | Moves the turtle forward by the specified amount                                                                                 |
| backward |      amount      |  backward(100) | Moves the turtle backward by the specified amount                                                                                |
|   right  | angle in degrees |    right(45)   | Turns the turtle clockwise by the specified angle                                                                                |
|   left   | angle in degress |    left(45)    | Turns the turtle counter clockwise by the specified angle                                                                        |
|   color  |     colorname    |  color("red")  | Sets the color for drawing. Use "red", "black", etc.  Here's a list of all the colors.                                           |
|   shape  |     shapename    | shape("arrow") | Should be "arrow", "classic", "turtle", or "circle"                                                                              |
|   speed  | number from 0-10 |    speed(0)    | Determines the speed at which the turtle moves around the window. 1 for slowest, 3 for normal speed, 10 for fast, 0 for fastest. |
|  pendown |       None       |    pendown()   | Puts down the turtle/pen so that it draws when it moves                                                                          |
|   penup  |       None       |     penup()    | Picks up the turtle/pen so that it doesn’t draw when it moves                                                                    |
| pensize  |       width      |   pensize(4)   | Sets the width of the pen for drawing                                                                                            |

### Error and bugs
While trying this out, you may come across errors or bugs, do not fear!
Write the issue down, and we can talk about it during class. Try to
figure out whether your bug is a:
{{< columns >}}
**Programmatic error** (which happens when the program does something different than what
you wanted. Remember that this happened when we set the angle to the wrong number)

<--->

**Syntax error** (which happens when the program crashes because the program cannot be
understood by the computer. Remember that this happened when we forgot a parentheses).

{{< /columns >}}


