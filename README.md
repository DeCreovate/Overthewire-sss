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

bandit3:
