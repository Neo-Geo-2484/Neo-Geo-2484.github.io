---
layout: post
title: Week 3 OTW Homework
published: true
---

Reference : https://overthewire.org/wargames/bandit/

Platform Used : Oracle VM Virtual Box Running Kali 


Self assessment:

This is a challenging, but fun assingment.I did my best to follow OTW directions,reasearch and use the commands tthey suggested. I did use a walkthough at times. I did get stuck a lot having to restart the terminal.I know by the end of this semester my Lunix experience will be leaps and bounds better. Just with this project I am seeing it more clearly. Prior to this class I did a breif intro to power shell and even more breif tutorial on umbntu.


			Level 0	
            
Directions:Log in using SSH on port 2220 username bandit0, 

Command: ssh bandit0@bandit.labs.overthewire.org -p 2220

Password Used:bandit0

---------------------------------
        
        
        	Level o-1

Directions:find the password for lv 2 in the readme file, found in the home directory 

Commands: ls - gave  readme

cat readme - gives pass

ssh bandit1@bandit.labs.overthewire.org -p 2220

Password Used: boJ9jbbUNNfktd78OOpsqOltutMc3MY1



Enjoy your stay ! bandit1 and pass worked

--------------------------------

			Level 1-2

Directions: while loggin in as bandit1 find pass in file called - which is in home directory. cat, ls , cat - do not work.


Commands: less ./- brought up the pass below, but then I get stuck on (END) had to reopen terminal and input below creds, it works I am off to the next lv:

user ssh bandit2@bandit.labs.overthewire.org -p 2220
Password Used:CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9


google Refrence:
on use of - 
What is dashed filename?
Usage of dash (-) in place of a filename
For a command, if using - as an argument in place of a file name will mean STDIN or STDOUT

--------------------------------

			Level 2-3

Directions: password for the next level is stored in a file called spaces in this filename located in the home directory

Command: ls- spaces in this filename
\spaces in this file name - bash: spaces: command not found
cat "spaces in this filename" - works and gives below pass

User ssh bandit3@bandit.labs.overthewire.org -p 2220

Password Used:UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK 

To to use files with spaces you can either use the escape character or youse the double quotes. \ is called escape character, used to not expansion of space, so now bash read the space as part of file name.

Google Refernece:
To to use files with spaces you can either use the escape character or youse the double quotes. \ is called escape character, used to not expansion of space, so now bash read the space as part of file name.


--------------------------------

			Level 3-4

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

Password Used: pIwrPrtPN36QITSp3EQaw936yaFoFgAB


--------------------------------

			Level 4-5

Directions:

Command: 

Password Used: 

--------------------------------

			Level 5-6

Directions:

Command: 

Password Used: 

--------------------------------

			Level 6-7

Directions:

Command: 

Password Used: 


--------------------------------

			Level 7-8

Directions:

Command: 

Password Used: 

--------------------------------

			Level 8-9

Directions:

Command: 

Password Used: 

--------------------------------

			Level 9-10

Directions:

Command: 

Password Used: 

--------------------------------

			Level 10-11

Directions:

Command: 

Password Used: 

--------------------------------

			Level 11-12

Directions:

Command: 

Password Used: 

--------------------------------

			Level 12-13

Directions:

Command: 

Password Used: 

--------------------------------

			Level 13-14

Directions:

Command: 

Password Used: 

--------------------------------

			Level 14-15

Directions:

Command: 

Password Used: 

--------------------------------

			Level 15-16

Directions:

Command: 

Password Used: 

--------------------------------

			Level 16-17

Directions:

Password Used: 

--------------------------------

			Level 17-18

Directions:

Password Used: 

--------------------------------

			Level 18-19

Directions:

Password Used: 

--------------------------------

			Level 19-20 

Directions:

Password Used: 


