# Overthewire-sss
step by step guide on how to solve over the wire war games challenge

**Overthewire**
**bandit0- finish** 
 **bandit0 : ssh bandit0@bandit.labs.overthewire.org -p 2220**
 ls then cat the readme file
 **bandit0 flag: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR**

**Bandit1**
**ssh bandit1@bandit.labs.overthewire.org -p 2220**

starts with - → use ./filename or -- filename.(
Contains shell special characters (*, ?, $, !, #, spaces, etc.) → quote or escape the filename. examples
cat '#file'
cat '$file'
cat '*file' or just escape using
./$file
used the command cat ./-  to get the flag
**bandit1 flag :PK8fYLZg2hnHSz83plBL1iEPKdD3QToB**

**bandit2:**
**ssh bandit2@bandit.labs.overthewire.org -p 2220**

Because the filename begins with -, cat might think it's an option (like --help). Prefixing it with ./ tells cat it's a file in the current directory. so using
**cat "./--spaces in this filename--"**
to get our flag

**bandit3: xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq**
file name was hiding from u
got it after opening the inhere directory
used ls -a to open hidden files
then cat the ...hiding from you file to get our flag.

**bandit4:6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG**

here we are looking for the only human redable file that is ASCII text

used file ./* to expose all the file types and identified my ascii text. which was my file07 then i used cat "./-file07" to open the file because it started with a - to make it look like its in the main directory.


**bandit5:pXa26xhMWaC2SvDotA4r9EgZkulOeSBW**

**file . -type f -size 1033c ! -executable**

file → Search for files.
. → Start searching in the current directory (inhere).
-type f → Only look for files (not directories).
-size 1033c → Find files that are exactly 1033 bytes (c means bytes).
! -executable → The file is not executable, so ignore executable files.
