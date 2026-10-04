# linux-bandit

Hi, this is my personal Linux learning notebook.

I'm building my foundation for a career in AI/ML research and engineering, and almost all of that work happens on Linux machines, servers and the command line. So I'm learning it properly: first by writing my own notes on the fundamentals, then by putting those commands to work on the [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) wargame.

Everything here is written in my own words, as I learn it. It's a work in progress, and I keep adding to it.

## What's in this repo

| File | What it is |
| :--- | :--- |
| [`Linux.md`](Linux.md) | My Linux notes: how the system works and the commands I use, with short comments on what each one does |
| [`Bandit.md`](Bandit.md) | My Bandit journey, level by level (0 to 33): how I logged in and the commands that got me to the next level |

## What I learned in `Linux.md`

- What Linux actually is, how GNU fits in, and what a VPS and WSL are
- Moving around and managing files: `ls`, `cd`, `mkdir`, `touch`, `cp`, `mv`, `rm`
- Reading and editing files: `cat`, `head`, `tail -f`, `less`, `nano`
- Redirection and pipes: `>`, `>>`, `2>`, `|`, `sort`
- Searching: `grep` and `find`, which I used the most
- Permissions, users and groups: `chmod`, `chown`, `su`, `sudo`
- Making the shell my own: aliases, environment variables, `PATH`, `.bashrc`, shortcuts, history
- Automating things with Bash scripts and `cron`

## What I practiced in `Bandit.md`

Bandit is where the notes turned into real skills. Working through it, I got hands-on with:

- **Levels 0-12:** navigating, hidden files, `find`, `grep`, `sort | uniq`, `strings`, Base64 and ROT13
- **Level 13:** unpacking layers of compressed files with `xxd`, `gzip`, `bzip2` and `tar`
- **Levels 14-20:** SSH keys, `scp`, `nc`/`ncat`, `nmap`, `diff`
- **Levels 21-25:** cron jobs, writing small scripts, brute-forcing a PIN
- **Levels 26-33:** escaping a restricted shell through `vim`, and Git (clone, log, branches, tags, push)

## Why I'm sharing this

Writing things down is how I make them stick, and keeping it on GitHub lets me track my progress. If it helps someone else starting out, even better.

## A note before you read `Bandit.md`

It contains my complete solutions. If you're planning to play Bandit yourself, try each level on your own first and come back here only when you're stuck. That's where the learning happens.

## Credits

Thanks to [OverTheWire](https://overthewire.org/) for building Bandit.