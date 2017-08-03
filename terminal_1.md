## Terminal Basics

The terminal is a command line interface where you can type and execute various commands. The Terminal is used to complete various tasks, like managing various software, running scripts, and writing code. Proficiency with the terminal is essential to being able to quickly navigate your system and projects. There are a lot of names for the Terminal, including console, shell, and command line, but they all refer to the same thing. For this guide, we will stick with "terminal".

### Getting started with Terminal

If you use a Mac or a Linux system, a terminal app is already installed and ready to be used! If you're on Windows, we recommend downloading [cmder](http://cmder.net/), which is a console emulator for Windows. If you're feeling fancy, you can use [Bash on Ubuntu on Windows](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide), but either will give you the same experience for learning terminal.

### Terminal Commands

Since terminal is really just a way to interpret commands, it's useful to know, and even memorize some common commands. Once you start using them regularly, you will naturally remember them. The following are some useful commands that you should know:

| Command | Description                              |
| ------- | ---------------------------------------- |
| pwd   | Prints your current working directory (the folder your terminal is in) |
| ls    | Lists all files in your current working directory |
| cd    | Allows you to **c**hange **d**irectories, (eg. `cd Documents`). Using `cd ..` will take you one directory above your current working directory. |
| mkdir | **M**akes a **dir**ectory, eg. `mkdir newfolder` will create a folder with the name "newfolder" in your current working directory |
| cp    | **C**o**p**ies a file, eg. `cp fileToCopy copiedFile`. Can also be used to copy an entire folder to another location |
| mv    | **M**o**v**es a folder, eg. `mv photos ../photos` moves the folder `photos` up one directory. this can also be used to rename a folder, eg `mv photos videos` renames the `photos` folder to `videos` |

Of course, there are *hundreds* of commands that you can use, and each command can have "flags". A flag is a way to add an option to a command, and comes in this form: `command -flag1 -flag2`, so for example, `ls -a -l` would have two flags, which modify how `ls` works. I can even combine them into one flag, like so: `ls -al`.

**Bash** (the software that runs "inside" terminal), also has a set of features that come in handy. When trying to change a folder, many people type out the entire folder name. You can use `Tab` to type in the first couple letters of the folder or file you're trying to modify, and Bash will automatically autocomplete the name, saving you a *lot* of time. To get to your previous commands, you can use the up arrow  (`↑`) key to go through your history, and the down (`↓`) key to go to your next commands. To kill your current process (eg running a script, `python script.py`), use `Ctrl`+`C`.

Many people replace Bash with alternatives, like [zsh](http://www.zsh.org/) or [fish](https://fishshell.com/), but this is totally optional. Different shells come with different features, like theming to make your terminal pretty, or a set of plugins. For most use cases, Bash is sufficient, but we encourage you to explore alternatives.
