---
layout: post
title: '                  Week 3 OTW Bandit'
published: true
---

**Reference :** 

1) https://overthewire.org/wargames/bandit/

2) Google.com


**Walkthrough help:**

1) https://www.youtube.com/watch?v=HR_0vVGtOYE

2) Google.com


**Platform Used :**

1) Oracle VM Virtual Box Running Kali 


**Summary:**

This is was a challenging, but fun assingment. I did my best to follow OTW directions, reasearch and use the commands they suggested. I did use a walkthough at times. I did get stuck a lot having to restart the terminal. I know by the end of this semester my Lunix experience will be leaps and bounds better. Just with this project I am seeing it more clearly. Prior to this class I did a breif intro to power shell and even more breif tutorial on Ubuntu.



**Level 0:**
            
Directions:Log in using SSH on port 2220 username bandit0, 

Command: ssh bandit0@bandit.labs.overthewire.org -p 2220

Password Used:bandit0



        
**Level 0-1:**

Directions:find the password for lv 2 in the readme file, found in the home directory 

Commands: ls - gave  readme

cat readme - gives pass

ssh bandit1@bandit.labs.overthewire.org -p 2220

Password found: boJ9jbbUNNfktd78OOpsqOltutMc3MY1

Enjoy your stay ! bandit1 and pass worked





**Level 1-2:**

Directions: while loggin in as bandit1 find pass in file called - which is in home directory. cat, ls , cat - do not work.


Commands: less ./- brought up the pass below, but then I get stuck on (END) had to reopen terminal and input below creds, it works I am off to the next lv:

user ssh bandit2@bandit.labs.overthewire.org -p 2220
Password found:CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9


google Refrence:
on use of - 
What is dashed filename?
Usage of dash (-) in place of a filename
For a command, if using - as an argument in place of a file name will mean STDIN or STDOUT



Level 2-3:

Directions: password for the next level is stored in a file called spaces in this filename located in the home directory

Command: ls- spaces in this filename
\spaces in this file name - bash: spaces: command not found
cat "spaces in this filename" - works and gives below pass

User ssh bandit3@bandit.labs.overthewire.org -p 2220

Password found:UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK 

To to use files with spaces you can either use the escape character or youse the double quotes. \ is called escape character, used to not expansion of space, so now bash read the space as part of file name.

Google Refernece:
To to use files with spaces you can either use the escape character or youse the double quotes. \ is called escape character, used to not expansion of space, so now bash read the space as part of file name.



Level 3-4:

Directions: password for the next level is stored in a hidden file in the inhere directory.

Command: ls- shows in here 
cat inhere - says its a directory
cd inhere
find - ./- hidden 
got stuck and it gave me end so I restarted w creds and tried 
cat inhere
cat inhere "hidden" none worked
then I used :
ls -la inhere and it brought up some permissions info
it also shows a .hidden

from here:

i added cat

cat inhere/.hidden - reveals pass


ssh bandit4@bandit.labs.overthewire.org -p 2220
Password found: pIwrPrtPN36QITSp3EQaw936yaFoFgAB




Level 4-5:

Directions: password for the next level is stored in the only human-readable file in the inhere directory

Commands: 
ls - inhere
cat inhere- directory 
cat inhere-file 
cat "inhere" 
ls
ls -la inhere
cat- lost and had to restart terminal 

cat inhere/ -file01 - invalid 
cat inhere/ -file00 - invalid
cat inhere/ -file06 - invalid
cat inhere/ -file04 - invalid
cat inhere/ -file07 - invalid
cat-help - not found 
file in;here; 00-07 - no directory 

ls 
cat inhere/-file07 - worked 



"reset"
ssh bandit5@bandit.labs.overthewire.org -p 2220
Password found: koReBOKuIDDepwhWk7jZC0RTdopnAYKh




Level 5-6:

Directions:password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable

Command: ls - inhere
ls-la inhere - 21 files 
maybehere folders 00-19

using find 

find -size 1033c - ./ inhere/maybehere 07/.file2
cat inhere/maybehere 07/.file2 - no directory 
./ inhere/maybehere07/.file2- gives pass


ssh bandit6@bandit.labs.overthewire.org -p 2220
Password found: DXjZPULLxYr17uwoI01bNLQbtFemEgo7




Level 6-7:

Directions:password for the next level is stored somewhere on the server and has all of the following properties: 

owned by user bandit7
owned by group bandit6
33 bytes in size

Command: 
ls
find
-size
and 33b
grep bandit7 - error and i need to log back in 

find / - this listed 100= entrys and I dont think that was right 

find / -size 33c -user bandit7 -group bandit6 

this produced another log found alot of premisson denied. 1 log shows path and has password after so lets use it :

cat /var/lib/dpkg/info/bandit7.password

ssh bandit7@bandit.labs.overthewire.org -p 2220
Password found: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs





Level 7-8:

Directions:password for the next level is stored in the file data.txt next to the word millionth

Command: grep data.txt
grep millionth
grep
grep millionth /data.txt
ls

cat data.txt | grep -i millionth




ssh bandit8@bandit.labs.overthewire.org -p 2220
Password found: cvX2JJa4CFALtqS87jk27qwqGhBM9plV



Level 8-9:

Directions:The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

Command: grep data.txt  - had to restart terminal 

ls

cat eror had to re start terminal

cat data.txt - huge amount of text

sort data.txt

sort data.txt | uniq -u



Password found: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR





Level 9-10:

Directions:password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

Command: ls data.txt

cat ls.data.txt

strings data.txt | grep '=' 

Password found: 



Level 10-11:

Directions:

Command: 

Password found: 




Level 11-12:

Directions:

Command: 

Password Used: 




Level 12-13:

Directions:

Command: 

Password Used: 




Level 13-14:

Directions:

Command: 

Password Used: 




Level 14-15:

Directions:

Command: 

Password Used: 




Level 15-16

Directions:

Command: 

Password Used: 





Level 16-17

Directions:

Password Used: 




Level 17-18

Directions:

Password Used: 





Level 18-19

Directions:

Password Used: 






Level 19-20 

Directions:

Password Used: 


