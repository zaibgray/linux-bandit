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

### Navigation & Files

Before you can do anything else on Linux, you need to move around and manage files — this is the muscle memory you'll build first.

- cd folder -> move into a folder
- cd .. -> move up one folder
- ls -la -> list all files, including hidden ones, with details (size, owner, permissions)
- pwd -> show where you currently are
- cp source dest -> copy a file or folder
- mv old new -> move or rename a file
- rm -i file -> delete a file (asks "are you sure?" first — safer than plain rm)
- mkdir -p a/b/c -> create a folder, and any missing parent folders, in one go
- find . -name "*.py" -> search the current folder (and subfolders) for files matching a pattern
- grep -r "text" . -> search inside files for a piece of text

### Viewing Files

You often don't want to open a full editor just to peek at a file — these let you read without editing.

- cat file -> dump the whole file to the screen (good for short files)
- less file -> open a file you can scroll through (press q to quit)
- head file -> show the first 10 lines (useful for checking a file's shape)
- tail -f file -> show the last lines and keep watching for new ones — the go-to for live logs

### Permissions

Linux is strict about who can read, write, or run a file. These commands change that.

- chmod +x file -> make a file runnable (e.g. a script)
- chmod 755 file -> set exact permissions: owner can read/write/run, everyone else can read/run
- chown user:group file -> change who owns a file
- sudo command -> run one command with admin rights (asks for your password)

### Processes & System

Everything running on your machine is a "process". These commands let you see and control them.

- ps aux -> list every running process, right now, as a snapshot
- top -> same idea, but live and updating (press q to quit)
- kill -9 PID -> force-stop a process by its ID number (get the ID from ps aux or top)
- df -h -> show how much disk space is used/free, in human-readable sizes (GB, MB)
- du -sh * -> show the size of each file/folder in the current directory
- free -h -> show how much RAM is used/free

### Networking

For talking to other machines — servers, websites, your VPS.

- ping host -> check if a machine is reachable (e.g. ping google.com)
- curl url -> fetch a URL and print the response — handy for testing APIs
- ssh user@host -> log into a remote machine's terminal
- scp file user@host:/path -> copy a file to a remote machine over SSH
- ip a -> show your machine's network interfaces and IP addresses

### Package Management

How you install and remove software, the Linux way (instead of downloading .exe files).

- sudo apt install pkg -> install a package (Debian/Ubuntu)
- sudo apt remove pkg -> uninstall a package
- apt list --installed -> see everything currently installed

### Compression

Bundling files together, or unpacking bundles someone sent you.

- tar -czvf out.tar.gz folder/ -> compress a folder into a single .tar.gz file
- tar -xzvf file.tar.gz -> extract a .tar.gz file back into its contents
- unzip file.zip -> extract a .zip file

### Shell Productivity

Small habits that save real time once they're automatic.

- history -> show a list of commands you've typed before
- !! -> instantly re-run your last command (great after sudo !!)
- Ctrl+R -> start typing to search your command history
- alias ll='ls -la' -> create a shortcut for a long command (save this line in ~/.bashrc to make it permanent)
- command1 && command2 -> run command2 only if command1 succeeded
- command1 | command2 -> pipe: feed the output of command1 into command2

### Git

Version control — tracking changes to your code over time.

- git status -> see what's changed since your last commit
- git add . -> stage all changes, ready to commit
- git commit -m "message" -> save a snapshot of staged changes
- git push -> upload your commits to the remote (e.g. GitHub)
- git pull -> download the latest commits from the remote
- git log --oneline -> see commit history, one line per commit