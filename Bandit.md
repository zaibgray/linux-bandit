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

The pipe operator (|) takes the output of one command and automatically feeds it as the input into the next command, like a pipeline connecting two tools.

Login
- ssh -p 2220 bandit8@bandit.labs.overthewire.org
- password: VR1ljMayciFxbnUokuQmJFw6QC9VKtub

Solution

- ls
- sort data.txt | uniq -u
- password: EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl
- logout

## Level 10

Login
- ssh -p 2220 bandit9@bandit.labs.overthewire.org
- password: EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl

Solution

- ls
- strings filename.txt | grep -E '^={2,}'

  - strings filename.txt: Extracts all readable text from the file.

  - |: Feeds that text into the next command.grep 

  - -E: Searches the text using advanced rules.
  - '^={2,}': Matches only lines starting with == or more.

- password: B0s2khmbT9u0geKuOoVGW3JZKhndE3BG
- logout

## Level 11

Login
- ssh -p 2220 bandit10@bandit.labs.overthewire.org
- password: B0s2khmbT9u0geKuOoVGW3JZKhndE3BG

Solution

- ls
- base64 -d data.txt
- password: pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro
- logout

## Level 12

Login
- ssh -p 2220 bandit11@bandit.labs.overthewire.org
- password: pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro

Solution

- ls
- strings data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
  - [ROT13](https://en.wikipedia.org/wiki/ROT13)
  - This command shifts every letter forward by 13 positions in the alphabet (ROT13) to instantly encode or decode rotated text.
- password: GROozWPO8QyN0mGrjUkID0WCYkZiQxrN
- logout

## Level 13

Login
- ssh -p 2220 bandit12@bandit.labs.overthewire.org
- password: GROozWPO8QyN0mGrjUkID0WCYkZiQxrN

Solution

- mktemp -d -> creating directory in /tmp
- cp data.txt /tmp/tmp.L4eY96Xcq0 -> making copy of data
- cd /tmp/tmp.L4eY96Xcq0 -> opening tmp directory
- mv data.txt data.hex ->  changing txt to hex
- xxd -r data.hex data ->  converting hexdump to orginal binary file
- file data -> compression format is gzip
- mv data data.gz -> changing data to gz
- gunzip data.gz
- mv data data.bz2
- bunzip2 data.bz2
- mv data data.tar
- tar -xf data.tar
- file * -> for each file
- tar -xf data5.bin
- file *
- mv data6.bin data6.bz2
- bunzip2 data6.bz2
- file *
- tar -xf data6
- file *
- mv data8.bin data8.gz
- gunzip data8.gz
- file *
- cat data8
- passoword : qQYQiHOBPR8zR61qxYqX45quvihF2uzk
- logout


## Level 14

Login
- ssh -p 2220 bandit13@bandit.labs.overthewire.org
- password: qQYQiHOBPR8zR61qxYqX45quvihF2uzk

Solution

- ls
- scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private ~/Desktop/
- chmod 600 ~/Desktop/sshkey.private
- ssh -i ~/Desktop/sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
- password: aaWecNkG4FhxJQxz07uiwzVP6bJiYS65

## Level 15

Login

- ssh -p 2220 bandit14@bandit.labs.overthewire.org
- password: aaWecNkG4FhxJQxz07uiwzVP6bJiYS65

Solution

- nc localhost 30000
- aaWecNkG4FhxJQxz07uiwzVP6bJiYS65
- password: pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7
- exit

## Level 16

Login

- ssh -p 2220 bandit15@bandit.labs.overthewire.org
- password: pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7

Solution

- ncat --ssl localhost 3000l
- enter password of bandit15
- password: kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V

## Level 17

Login

- ssh -p 2220 bandit16@bandit.labs.overthewire.org
- password: kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V

Solution

- nmap -p 31000-32000 localhost
- nmap -sV -p 31000-32000 localhost
- ncat --ssl localhost 31790 -> port 31790 has ssl/unknown
- enter password: kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V
- you will get key -> copy it
- exit
- nano b17.key -> ctrl+o, enter, ctrl+x
- chmod 600 b17.key
- ssh -i b17.key bandit17@bandit.labs.overthewire.org -p 2220

### Level 18

Login

- ssh -i b17.key bandit17@bandit.labs.overthewire.org -p 2220

Solution

- ls
- diff passwords.old passwords.new
- password: OQxXZjELndr90zuhOTDYBEomI0SZITXI


## Level 19

Login

- ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat readme"
- password: OQxXZjELndr90zuhOTDYBEomI0SZITXI

Solution

- password: KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI

## Level 20

Login

- ssh -p 2220 bandit20@bandit.labs.overthewire.org
- password: KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI

Solution
