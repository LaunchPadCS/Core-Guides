## Vim Basics

The `vim` program is a text editor that works from inside the terminal. There are a lot of competing text editors, but vim is a very popular (and powerful) choice. It's a little tricky to pick up at first, but it's really worth learning.   

### Vim Modes
Vim has several different modes that all work differently, but there's only three that are important to understand right away.

When you first open the editor, you'll be using `normal mode`. Despite the name, this mode doesn't work like you might normally expect. Your keys are all treated as shortcuts in the mode and will not actually type text.

If you tap `i` from normal mode, you'll enter `insert mode`. This mode works like you might expect. Typing letters here will add those letters to your file, and you can use the arrow keys to move around. When you're done typing, you press `ESC` to return to normal mode.

If you tap `:` while in normal mode, you'll enter `command mode` (also called `Ex-mode`). This is a mode that allows you enter more complicated sets of commands. You can press `ESC` to return to normal mode and cancel the command you were typing. You can press `ENTER` while in command mode to execute whatever command you typed.


### Saving & Exiting Vim
To save a file, you press `:` to enter command mode. In vim, the `w` command is what lets you save the file. So after typing `:`, you can enter `w` and then hit enter to confirm.

Closing a file works pretty much the same way. You press `:` to enter command mode, then type `q`, then hit enter. If you try to quit without saving, vim will warn you that you still have unsaved changes. If you want to discard those changes and quit anyways, you can use the `q!`  command instead.

Finally, you can save and quit in a single action using the `wq` command.


### Some Handy Commands
The real power in vim comes from the incredible number of powerful commands and shortcuts. Unlike most editors, you can actually combine these commands together to run more complex actions. Remember that all these actions are preformed while in `normal mode`.

Here's some basic shortcuts that are handy for moving around the file:

key|use
----|---|
w|Skip to the next word|
b|Skip backwards to the last word|
e|Jump to the end of this word
0|Jump the start of the current line
$|Jump to the end of the current line
j|Jump to the next line
k|Jump up to the previous line

Here's another cool trick- every one of those previous shortcuts (except `0` and `$`) can be combined with a number. For example, `5j` will jump 5 lines forward, and `15b` will jump 15 words backwards.

###Moving forward...
We're about to go a little more in-depth. If you want to learn more about vim commands, take a look at the section below, but don't feel like you need understand everything. Vim is famous for being hard to learn, and you don't need to understand all the little details in order to use vim.


#### Some fancier commands
Still here? Alright then, here's a few fancier commands:


You can you use `yy` to copy a line (think y for "yank"), and `p` to paste. You can also use `dd` to cut a line instead of copying. You can also combine those commands with a number to copy/cut that number of lines. For example `y5y` copies 5 lines.

You can use use the `/` command to start searching. After typing the `/`, you just enter the word you want to search for and hit enter. Vim will jump to the first result, but you can tap `n` to move through each result until you find what you want. You can also use `?` instead of `/` if you want to search backwards instead of forwards.

To switch to another file, you can use the `:e .` command (including the period). This will open a list of all the files in your current directory. From there, you can use the arrow keys to navigate to another file and press enter to open it. If you have a lot of files open, you can always run `:ls`to view a list of all the files you have currently open.

Last (but certainly not least), you can always type `u` to undo your last command.

#### Mixing and matching commands
The real power in vim comes from being able to combine commands. A great way to think about this is to picture combining a verb (the action) with a noun (the target). For example, `yy` is saying to yank (the action) the current line (the target).  

Here's some common "nouns" in vim:

key|noun
----|---|
p|Paragraph|
s|Sentence
w|Word
t|XML/HTML tag|
'|Single quote string|
"|Double quote string|
(|A function wrapped in ( |
{|A function wrapped in { |
[|A function wrapped in [|


This is a little hard to see without some examples, so let's write some.

You can use the  `i` key to represent "inside", followed by a "where" noun. So `ip` would represent "inside this paragraph", and `is` represents "inside this sentence".

Say you wanted to cut some text. You could type `dd` to just cut the entire line. But what if you wanted to just cut the sentence your cursor is on? In that case, you could type `dis` to say "cut inside this sentence". Or if you were working on a java function wrapped in `{}` marks, you could type `di{` to cut the entire thing.

We've barely scratched the surface here, but hopefully you can start to see why vim is so powerful. If you master vim, you can specify insanely complex commands and fly through your files like a pro. For most of us, knowing the basics of vim will be enough.

### Recommended Reading
[This](https://www.youtube.com/watch?v=wlR5gYd6um0) video is an amazing resource for vim. It gives a great overview of how the vim language works. 
