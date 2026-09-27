# Bandit

## Level 0

- [ssh](https://itsfoss.com/ssh-to-port/)
- ssh -p portnumber user@ip-addres
- pssword

Login

- ssh -p 2220 bandit0@bandit.labs.overthewire.org
- password: bandit0

## Level 1

Commands you may need to solve this level

- ls , cd , cat , file , du , find

Solution

- ls
- cat readme
- password: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
- logout

## Level 2

Login

- ssh -p 2220 bandit1@bandit.labs.overthewire.org
- password: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR

Solution

- ls
- cat < -
- password: PK8fYLZg2hnHSz83plBL1iEPKdD3QToB 
- logout

## Level 3

Login

- ssh -p 2220 bandit2@bandit.labs.overthewire.org
- password: PK8fYLZg2hnHSz83plBL1iEPKdD3QToB

Solution

- ls
- cat -- "--spaces in this filename--"
- password: 7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME
- logout

## Level 4

Login

- ssh -p 2220 bandit3@bandit.labs.overthewire.org
- password: 7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME

Solution

- ls
- cd inhere
- ls -alh
- cat ...Hiding-From-You
- password: xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
- logout

### Level 5

Login

- ssh -p 2220 bandit4@bandit.labs.overthewire.org
- password: xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq

Solution

- ls
- cd inhere
- find . -type f -exec file {} +
- look for This looks at the actual contents of the files and labels them (e.g., "ASCII text", "UTF-8 Unicode text", or "ELF 64-bit binary").
- cat < -file07
- password: 6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
- logout

### Level 6

Login

- ssh -p 2220 bandit5@bandit.labs.overthewire.org
- password: 6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG

Solution

- ls
- cd inhere
- find . -type f -size 1033c ! -executable -exec ls -lh {} +
  - This command searches the current directory (find .) for regular files (-type f) that are exactly 1033 bytes (-size 1033c), lack execute permissions (! -executable), and displays their details (-exec ls -lh {} +) in a human-readable format.
- cd maybehere07
- ls -alh
- cat < .file2
- password: pXa26xhMWaC2SvDotA4r9EgZkulOeSBW
- logout

## Level 7

Login

- ssh -p 2220 bandit6@bandit.labs.overthewire.org
- password: pXa26xhMWaC2SvDotA4r9EgZkulOeSBW

Solution

- ls
- find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
  - This command searches the entire server (find /) for files owned by user bandit7 (-user bandit7) and group bandit6 (-group bandit6) that are exactly 33 bytes (-size 33c), while silencing permission errors (2>/dev/null).
- cat < /var/lib/dpkg/info/bandit7.password
- password: Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3
- logout

## Level 8

| Command | One-Line Description |
| :--- | :--- |
| **`man`** | Displays the reference manual for command-line utilities. |
| **`grep`** | Searches files for text lines matching a specified pattern. |
| **`sort`** | Sorts lines of text files alphabetically or numerically. |
| **`uniq`** | Identifies or removes duplicate lines from a sorted file. |
| **`strings`** | Finds and prints human-readable text hidden inside binary files. |
| **`base64`** | Encodes or decodes text and files into Base64 format. |
| **`tr`** | Translates, replaces, or deletes specific characters from data streams. |
| **`tar`** | Bundles multiple files and directories into a single archive file. |
| **`gzip`** | Compresses or decompresses files into `.gz` format. |
| **`bzip2`** | Compresses files into `.bz2` format, offering higher reduction than gzip. |
| **`xxd`** | Generates a hexadecimal dump of binary data or reverses it back to binary. |

Login

- ssh -p 2220 bandit7@bandit.labs.overthewire.org
- password: Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3

Solution

- ls
- grep "millionth" data.txt
- password: VR1ljMayciFxbnUokuQmJFw6QC9VKtub
- logout

## Level 9

Login
- ssh -p 2220 bandit8@bandit.labs.overthewire.org
- password: VR1ljMayciFxbnUokuQmJFw6QC9VKtub

Solution

- ls