# Command Line Basics

If you opened up Terminal or Git Bash then you should see a window that looks
something like this:

![](img/shell1.png)

What you're looking at is the bash shell! Your shell will surely look different 
than mine, but all bash shells have the same essential parts. As you can see in
my shell it says `seans-air:~ sean$`. This string of characters is called the
**prompt**. You type command line commands after the prompt. The prompt is just
there to let you know that the shell is ready for you to type in a command.
Press `Enter` on your keyboard a few times to see what happens with the prompt.
Your shell should now look like this:

![](img/shell2.png)

If you don't type anything after the prompt and you press enter then nothing
happens, and you get a new prompt under the old prompt. The white rectangle 
after the prompt is just a cursor that allows you to edit what you've typed
into the shell. Your cursor might look like a rectangle, a line, or an
underscore, but all cursors behave the same way. After typing something into
the command line you can move the cursor back and forth with the left and right
arrow keys.

Don't you think your shell looks messy with all of those old prompts? Don't
worry, you're about to learn your first shell command which will clean your
shell up! Type `clean` at the prompt and then hit enter. Voila! Your command
line is back to how you started.

Every command line command is actually a little computer program, even commands
as simple as `clean`. These commands all tend to have the following structure:

```
[commnd] [options] [arguments]
```

Some simple commands like `clean` don't require any options or arguments.
Options are usually preceded by a hyphen (`-`) and they tweak the behavior
of the command. Arguments can be names of files, raw data, or other options
that the command requires. A simple command that has an argument is `echo`.
The `echo` command prints a phrase to the console. Enter `echo "Hello World!"`
into the command line so see what happens:


```bash
echo "Hello World!"
```

```
## Hello World!
```

We'll be using the above syntax for the rest of the book, where on one line there
will be a command that I've entered into the command line, and then below that
command the console output of the command will appear (if there is any
console output). You can use `echo` to print any phase surrounded by double
quotes (`""`) to the console.

## Navigating the Command Line

You've learned two command line commands which is pretty good! Before you learn
more commands we need to discuss how files and folders are organized on your
computer.

Computers are organized in a hierarchy of folders, where a folder can contain 
many folders and files. People who use Unix often refer to folders as 
directories and these terms are interchangeable. This directory hierarchy forms 
a tree, like the diagram below. We can use the command line to navigate these
trees on your computer.

![](img/musictree1.png)

As you can see in the image below, my Debussy directory is contained in my Music directory. This is the simplest case of how directories are structured.

![](img/musictree2.png)

The directory structure on most computers is much more complicated, but the 
structure on your computer probably looks something like this:

![](img/bigtree1.png)

There are a few special directories that you should be aware of on your 
computer. The directory at the top of this tree is called the root directory. 
The root directory contains all other directories, and is represented by a 
slash (`/`).

The home directory is another special directory that is represented by a tilde 
(`~`). Your home directory contains your personal files, like your photos, 
documents, and the contents of your desktop. When you first open up your shell
you usually start off in your home directory. Imagine tracing all of the 
directories from your root directory to the directory you're currently in. This
squence of directories is called a "path." The diagram below illustrates the
path from a hypothetical root directory to the home directory.

![](img/redtree.png)

This path can be written as `/Users/sean`

Open the command line if you closed it (either **Terminal** or **Git Bash**).
Your shell starts in your home directory. Whatever directory your shell is in
is called the **workig directory**. Enter the `pwd` command into your shell
to **p**rint the **w**orking **d**irectory.


```bash
pwd
```

```
## /Users/sean
```

You can change your working directory using the `cd` command. If you use the
`cd` command without any arguments then your home working directory is changed
to your home directory.

Enter `cd` into the command line and then enter `pwd`.


```bash
cd
pwd
```

```
## /Users/sean
```