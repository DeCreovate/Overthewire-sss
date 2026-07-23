 Overthewire-sss
step by step guide on how to solve over the wire war games challenge

**Overthewire**
**bandit0- finish** 
 **bandit0 : ssh bandit0@bandit.labs.overthewire.org -p 2220**
 ls then cat the readme file
 **bandit0 flag: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR**
 <img width="709" height="215" alt="image" src="https://github.com/user-attachments/assets/13e00f3c-9c3f-465a-927a-dc265a890e50" />

 

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
<img width="728" height="129" alt="image" src="https://github.com/user-attachments/assets/98ad97db-bedc-45de-9c15-27e9fdea97c9" />


**bandit2:**
**ssh bandit2@bandit.labs.overthewire.org -p 2220**

Because the filename begins with -, cat might think it's an option (like --help). Prefixing it with ./ tells cat it's a file in the current directory. so using
**cat "./--spaces in this filename--"**
to get our flag
<img width="725" height="120" alt="image" src="https://github.com/user-attachments/assets/c6707f27-3bbb-4964-abd5-3cc863d8f5d8" />


**bandit3: xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq**
file name was hiding from u
got it after opening the inhere directory
used ls -a to open hidden files
then cat the ...hiding from you file to get our flag.
<img width="725" height="174" alt="image" src="https://github.com/user-attachments/assets/3e313a79-14a4-42ee-9b50-ee7ab629c664" />


**bandit4:6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG**

here we are looking for the only human readable file that is ASCII text

used file ./* to expose all the file types and identified my ascii text. which was my file07 then i used cat "./-file07" to open the file because it started with a - to make it look like its in the main directory.
<img width="725" height="330" alt="image" src="https://github.com/user-attachments/assets/f718b454-2bc7-46e4-bb71-e4628a7cf6cb" />


**bandit5:pXa26xhMWaC2SvDotA4r9EgZkulOeSBW**

**find . -type f -size 1033c ! -executable**

file → Search for files.
. → Start searching in the current directory (inhere).
-type f → Only look for files (not directories).
-size 1033c → Find files that are exactly 1033 bytes (c means bytes).
! -executable → The file is not executable, so ignore executable files.
<img width="1169" height="274" alt="image" src="https://github.com/user-attachments/assets/c7378036-39c1-45b3-9717-2960c34f473b" />


**bandit6: Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3**

it was said that the password was  in a file somewhere in the sever in group bandit 6 and user bandit7 with size 33bytes

so i used the command
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
added 2>/dev/null to filter noise
c is used to represent bytes.

<img width="1169" height="274" alt="image" src="https://github.com/user-attachments/assets/868a1768-a7f1-48a8-ac71-c4a85ce55bbd" />
