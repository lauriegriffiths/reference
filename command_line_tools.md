# 50 Useful Command line tools

This is a document to support the video here:
(youtube link)

## Command Line Explanation
Introduction
Why use the command line?
The world of operating systems
What is Linux?
Shells and Bash

## Setting up Command Line
Linux 
Mac 
Windows (WSL)

## terminal basics
exiting,
tab completion
ctrl-r
ctrl-x ctrl-e
pressing up for past commands

## Basic commands
### whoami
The first command is very simple. `whoami` displays your username on the screen. Press enter to run the command.

This command might seem too simple but it can be very useful when you're logging into many different computers every day. 

After running the command press the up arrow to see commands you have run previously. You can look through many commands this way.

### man
`man` is short for manual. You can use this to find out more information about other commands.

Try running `man whoami`. You will see a simple explanation of the `whoami` command. To close the manual press `q`.

You can also try running the man command on itself.  `man man` will tell you more about the man command.

### clear
The `clear` command will clear everything on your screen. Try it out.

### pwd

`pwd` Up until now we've only run very simple commands. The `pwd` command will show you the directory you are in. Folders are divided with a forward slash `/`.

### touch

`touch` is a simple command to make an empty file. Give it the name of the file you want to create. `touch my_list.txt`

### ls

`ls` is short for 'list' and will show you a list of files and directories.  You can change what `ls` does using 'options'.  You write options with a hyphen and a letter after the command.  For example `ls -l` will show you more information including file sizes. 

### Command Line Options

`ls -a` will show you all files, including hidden files.  Hidden files start with a `.`.  Make a hidden file with `touch .hidden.txt`.  Now try looking for it with `ls`.  You can't see it. You need to use `ls -a`.

Command line options can be combined.  Writing `ls -al` will show you more information and include hidden files.  The order of options is not important, so `ls -la` will do the same thing.

### cd
So far we have stayed in one directory. To move to different directories use `cd`.  Write the name of the folder after the command, for example `cd notes` to change into a directory called notes. 

To move up to the parent directory, use `cd ..`. `..` is short for "the parent directory".  `.` is short for "the current directory".

### mkdir
Now we can navigate to different directories, let's make some more. Use `mkdir` to make a directory with a name you give it. For example `mkdir pictures` to make a directory called `pictures`.

### rmdir
You can remove (delete) directories with `rmdir` in the same way.  `rmdir` only removes empty directories. Some people like this so they don't accidentally remove many files. 

### rm
`rm` removes (deletes) files.  You can use the `-r` (recursive) option to remove directories and contents: `rm -r`.  `rm -i` (interactive) will ask you to confirm before you delete each file. 

### Command Line Expansion
We've learnt a few simple commands, let's do something useful. Imagine we have a folder containing hundreds of different files. We want to delete every text file, but leave all the image files. 

First, we use `ls` to look at the files. Now, we can use command line expansion to look at only the files ending with `.txt`.  `ls *.txt` will show only the text files.  `*` (asterisk) stands for "anything".  If we use the same pattern with `rm` we can delete every text file: `rm *.txt`. 

When you run this command every file ending in `.txt` will be deleted. Be careful!  This might be thousands of files!  

In the same way you can delete every file starting with the word `thumbnail`: `rm thumbnail*`. 

Sometimes you don't want to use expansion.  If you write `\*` it will be treated as an asterisk with no expansion.

### mv
`mv` is short for move.  Use it to move a file to a different location, or rename a file.

`mv data.txt AddressList.txt` will rename the file `data.txt` to `AddlistList.txt` in the same directory.

`mv data.txt notes` will move the file `data.txt`into the directory `notes`. Be careful! If `notes` doesn't exist then `data.txt` will be renamed.

### cp
`cp` is short for copy.  It is very similar to `mv` but you will end up with two files.

`cp data.txt extra.txt` will make a copy of `data.txt` in `extra.txt`.

### open / start / gnome-open

The `open` command is only on macs. It will open the file with the default program.  For example `open picture.jpg` will open the picture file using the mac Preview application. This is really useful for looking at images and audio.

`open .` will open the current directory in Finder. 

Open windows you can use `start` to do the same thing.

Linux can use `xdg-open`. 

### Review Questions
* Make a folder containing three files.
* Add another file to this folder and make it hidden.  
* Create a folder inside this folder and move one of the files inside it.
* Delete the folder you just created.
* Check the creation time of the hidden file you made (hint: use `ls`)

## Interactive mode

Some programs run in "interactive mode". This means you can type special commands (not command line commands) and get results interactively.

### bc

Try running the command `bc`.  Notice how your command prompt looks different.  If you try running commands like `ls` you won't get the regular result.  Interactive mode takes over the shell completely.  

`bc` is a calculator.  Try inputting basic calculations such as `25+36`.

`+` is addition, `-` subtraction, `*` multiplication and `/` is divison. Exponentiation is `^`.

Very large calculations are possible too.  Try `25^100`.  

To quit the `bc` program type `quit`. In general, if you get 'stuck' in a program, typing `quit`, `exit`, `q` or pressing ctrl-C will usually be enough to get you back to your familiar shell.

### less
`less` is a program for previewing the contents of files.  Use `less filename` to open a file using less and press spacebar to move down a whole page.  You can also use the arrow keys. 

Some other programs or scripts may use `less` to show you the contents of files.  You can use `q` to close less.  

### nano
`nano` is a simple text editor.  Open a file with `nano filename`.  Move around with the arrow keys and type to insert text.

The bar at the bottom shows you useful keyboard shortcuts.  `^X` means ctrl-X and will exit nano.  It will warn you if you haven't saved.  

### vim

`vim` is a much more powerful text editor. It has different modes for inserting text, selecting text and moving around a file.  A full explanation of `vim` is beyond the scope of this guide, but because it is often the default editor and because other tools often open it you need to know how to exit it.  Press the escape key to enter 'normal mode', then type `:q` and press enter.  

### python

Many programming languages come with interactive shells where you can execute commands from that programming language. One popular example is python.  

Run `python` to open a python terminal.  You can write any python code here. Try `max(51,123,312)`. The terminal should show you which number is largest.   

To exit the python terminal write `quit()` and press enter.

### Exercises 
* 


## Working with data in files

head
tail
date
cat
less
echo
PIPING

paste

wc
sort
uniq
redirecting standard output
grep
diff
tr
jot
yes
cut

## Interacting with your computer 
find
du
df
history
ps
top
kill
killall
jobs, bg, and fg
gzip
gunzip
tar
alias
xargs
ln

## Powerful utilities

awk
sed
imagemagick
ffmpeg
vim
hurl
csvkit


## Permissions and users
who
su
sudo
passwd
chown
Understanding permissions
chmod


nc

extras:
jq
tldr
gron
tig 
fpp

https://explainshell.com/explain?cmd=ls+-al

https://remysharp.com/2018/08/23/cli-improved

bat (better cat)

prettyping
fzf (fuzzy command line history search)

htop

diff-so-fancy

fd (better find)

ncdu


tree

https://community.coherentpdf.com/

fzf

pipe-rename

hexyl

delta

glow

miller

angle grinder 
https://github.com/rcoh/angle-grinder

jo
https://github.com/jpmens/jo

dateutils
https://github.com/hroptatyr/dateutils

fmt

pr

jid (json incremental digger for drilling down to specific jq commands)

musikcube (media player)

https://www.visidata.org/  

## Language stuff?
say

mecab

kakasi

nmap
