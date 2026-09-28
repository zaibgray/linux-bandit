# Linux

## What is Linux?

Linux is the kernel at the center of many operating systems. In everyday speech, people still call the
whole system "Linux". Both uses of the word are common.

- Hardware → Kernel → Shell → Programs

## GNU + Linux

The kernel needed programs around it:

- a compiler
- a shell
- file tools
- a C library.

GNU already had those. Combined with the Linux kernel, they made a complete operating system people could install
and use.

That pairing is why some people say GNU/Linux. In this handbook, "Linux" still means the whole system, unless a sentence is clearly about the kernel. The history is the useful part: Linux became usable
because a free kernel met a free userland.

Confirm you have that userland, not only a kernel:

- bash --version
- ls --version

## Whatis a VPS?

A VPS (Virtual Private Server) is a Linux machine you rent in the cloud. You reach it over SSH.
Commands you type run on that machine, not on your laptop.
It is cheap: billed for 1, 12, or 24 months. Pick Linux, not Windows. The OS has no license fee.
A VPS keeps your own computer clean. No local VM, no Linux install on the host. Use it for experiments, web apps, and cron jobs

## Whatis WSL?

WSL (Windows Subsystem for Linux) runs Ubuntu inside Windows without VirtualBox. Use it when you
only need a Linux terminal. Use VirtualBox when you want a full Ubuntu desktop.

## Commands

### Confirm You Are on Linux

- uname -a -> display Linux info
- cat /proc/version -> display kernal info
- hostnamectl -> display info about system
- cat /etc/os-release - display info about os-release
- whoami -> display current user
- pwd -> display the current directory
- hostname -> display the machine name

### Update System

- sudo dnf check-update -> Fedora Linux
- sudo apt update -> Debian Linux
- sudo pacman -Sy -> Arch Linux

### Getting Help

There are on-line manuals which gives information about most commands. The manual pages tell you which options a particular command can take, and how each option modifies the behaviour of the command. Type man command to read the manual page for a particular command.

- man pwd -> find out more about the pwd command
- man man

### Structure of Linux Command

- Command name + Options + Arguments
- cat -n abc.txt
- options are case sensitve
- options can be combined
- option short from: can -n abc.txt
- option long form: cat --number abc.txt

### man command

- man -> displays manual pages
  - NAME -> name and work
  - SYNOPSIS
        - [] -> Optional
        - ... -> Can give one or more options or arguments
        - without [] mean must need
  - DESCRIPTION -> give all the info about options and agruments

### ls, pwd and cd

- pwd -> print working directory
- ls -> list files
- cd -> change directory
- ls -a -> shows all file even hidden
- cd . -> same directory
- cd .. -> take you previous directory
- cd -l -> long formate of files
- cd -la -> grouping options
- cd -lah -> groupging with human-readable
- cd -laht -> sort with time
- cd -lahtr -> sort in reverse
- ls -l --sort=time -r
- ls -lahtS -> sort by size
- ls Music
- cd / -> root directory
- cd ~ -> home directory
- Absolute path
  - cd /home/zei/Documents
  - a path from root
- Relative path
  - cd Documents/

### Timestamps: Modification, Access and Change times

- ls -l -> shows modification time
- ls -lc -> shows change time
- ls -lu -> shows access time of the file

### File Management: mkdir, touch and file

- mkdir movies
- mkdir -p kids/animation/2021
- mkdir -p movies/{comedy,love} -> must not add space between ","
- man touch
- touch -> change file timestep
- touch -a -> change access time
- touch -m -> change modification time
- touch -> also make files
- touch london.txt names.txt love.txt
- touch can make any file (a.html, love.jpg, k.exe)
- without extention it make file witout extention
- touch a.html b.css. c.js
- touch 'hello world.txt'
- file -> display file's content type
- touch abc.txt
- cat << 'EOF' >> abc.txt
- mv abc.txt abc.mp4
- file abc.mp4 -> it will show ASCII text, beacuse it has text content not mp4

### Nano Text Editor

- Nano is a simple, easy-to-use text editor that operates within a terminal window.
- if a file is not there, it creates & open it.
- nano hell.txt
- Ctrl-O: write the current file to disk.
- Ctrl-X: close the current file buffer and exit the editor.
- Alt-G: got to a specific line number
- Ctrl-up-key: go to the start of the text
- Ctrl-down-key: go to the end of the text
- Ctrl-A: go to the start of the line
- Ctrl-E: go to the end of the line
- Ctrl + Shift + C : copy to global
- Ctrl + Shift + v : paste to global
- Alt + ^ copy the line/selected
- Ctrl-K: cut a line / selected
- Ctrl-U: Paste
- Alt+U: Undo
- Ctrl-W: Search for a string or a regular expression
- Ctrl + \ : replace a string

### File Management: Remove, Rename, Copy and Movie files and folders

