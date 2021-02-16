---
layout: post
title: '                  Week 3 OTW Bandit'
published: true
---










Week 3 Lab 

https://github.com/Neo-Geo-2484/Butte-CSCI-18/commit/9d008dd21d610f25bfd1fa2a816985b4883da1d1














**References:** 

1) https://overthewire.org/wargames/bandit/

2) Google.com


**Walkthrough help:**

1) https://www.youtube.com/watch?v=HR_0vVGtOYE

2) Google.com

Tools:

1) Rot13.com


**Platform Used :**

1) Oracle VM Virtual Box Running Kali 


**Summary:**

This is was a challenging, but fun assingment. I did my best to follow OTW directions, reasearch and use the commands they suggested. I did use a walkthough at times. I did get stuck a lot having to restart the terminal. Lv 12-13 most most challenging with the hexdum and using the ROT13 cypher was my most enjoyable level. 



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



**Level 2-3:**

Directions: password for the next level is stored in a file called spaces in this filename located in the home directory

Command: ls- spaces in this filename
\spaces in this file name - bash: spaces: command not found
cat "spaces in this filename" - works and gives below pass

User ssh bandit3@bandit.labs.overthewire.org -p 2220

Password found:UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK 

To to use files with spaces you can either use the escape character or youse the double quotes. \ is called escape character, used to not expansion of space, so now bash read the space as part of file name.

Google Refernece:
To to use files with spaces you can either use the escape character or youse the double quotes. \ is called escape character, used to not expansion of space, so now bash read the space as part of file name.



**Level 3-4:**

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




**Level 4-5:**

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




**Level 5-6:**

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




**Level 6-7:**

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





**Level 7-8:**

Directions:password for the next level is stored in the file data.txt next to the word millionth

Command: grep data.txt
grep millionth
grep
grep millionth /data.txt
ls

cat data.txt | grep -i millionth




ssh bandit8@bandit.labs.overthewire.org -p 2220
Password found: cvX2JJa4CFALtqS87jk27qwqGhBM9plV



**Level 8-9:**

Directions:The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

Command: grep data.txt  - had to restart terminal 

ls

cat eror had to re start terminal

cat data.txt - huge amount of text

sort data.txt

sort data.txt | uniq -u



Password found: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR





**Level 9-10:**

Directions:password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

Command: ls data.txt

cat ls.data.txt

strings data.txt | grep '=' 


ssh bandit10@bandit.labs.overthewire.org -p 2220

Password found: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk



**Level 10-11:**

Directions:password for the next level is stored in the file data.txt, which contains base64 encoded data

Command: ls
ls 
string data.txt | grep

base64 -d data.txt

Password found: 
IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR





**Level 11-12:**

Directions:password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positionsls
Rot 13 encrypton:


Command: ls - data.tx 
cat data.tx - displays contents 

using rot13.com copy contents from above and get password

Password found: 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu




**Level 12-13:**

Directions: password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

Command: ls - data.txt
cat data.txt - large amountof text 

mkdir /tmp/neogro - unable to create

mkdir -v /tmp/jeff123 - created 

xxd -r data.txt /tmp/jeff123/data.txt
cd /tmp/jeff123
ls

file new 

bzip2 -d new 

ls


zcat new.out  > newer

tar-xvf newer
file data5.bin

-xvf data5.bin
file date.bin
bzip -d data6.bin
ls
file data6.bin.out
tar -xvf data6.bin.out

file data8.bin
zcat data8.bin > newest
file newest
cat newest 

cp data.txt /tmp/jeff123

mv /tmp/jeff123/data.txt /tmp/jeff123/datacopy.txt

cat /tmp/jeff123/datacopy.txt - non human jibberish populated 

/temp/jeff123$ cat data8 

hexdump on wiki 

Password Used: 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL ( had to look up the walkthrough and use pass ) 




**Level 13-14:**

Directions:The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working o

Command: ls - sshkey.private 
cat sshkey.private - populated a lrage priavte key 

ssh -i sshkey.private bandit14@localhost 

type yes

copied " /etc/bandit_pass/bandit14" 

cat /etc/bandit_pass/bandit14 - populated password

Password Found:4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

-clear-



**Level 14-15:**

Directions:The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

Command: 

nc - added a cmd line:
nc - failed 

nc localhost 30000
BfMYroe26WYalil77FoDi9qh59eK5xNr



Password for bandit15 found: BfMYroe26WYalil77FoDi9qh59eK5xNr





**Level 15-16**

Directions:The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

Command: openssl s_client -conect localhost BfMYroe26WYalil77FoDi9qh59eK5xNr

openssl s_client -conect localhost30000 BfMYroe26WYalil77FoDi9qh59eK5xNr

openssl s_client -connect localhost:30001

BfMYroe26WYalil77FoDi9qh59eK5xNr


Password found: cluFn7wTiGryunymYOu4RcffSxQluehd





**Level 16-17**

Directions:The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.


Command: namp -sv localhost -p 31000-32000 command not found 


ls
nmap localhost
vi sshkey.private
namp -sV localhost -p 31000-32000 command not found
nmap local host populated some info
nmap loacalhost 31000-32000- populated more into 

openssl s_connect -connect localhost:31790 - invalid

openssl s_connect -connect localhost:997 invalid 

openssl s_client -connect localhost:31790-
SSL-Session:
    Protocol  : TLSv1.2
    Cipher    : ECDHE-RSA-AES256-GCM-SHA384
    Session-ID: A799E79F6641C6C289CB25186EB51043154049AB0006BF59A9588B0BB2A21932
    Session-ID-ctx: 
    Master-Key: 53F171B146C297F1E70B8F2F9E54E94EEE68D1710963C1806F0737FEB8D54494963BFFB80E98382A78537491D8AAF6AC
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 27 9a 97 c2 54 b0 3e e8-41 f1 14 05 fd 55 85 a7   '...T.>.A....U..
    0010 - 55 1d eb 5b 9d dc 27 c2-33 ff e5 c0 21 11 15 68   U..[..'.3...!..h
    0020 - 8a 9f 13 1c 44 c7 43 36-dc f2 f5 02 64 ea 37 b7   ....D.C6....d.7.
    0030 - 9d 7a ca d1 68 7c 4c cd-cd 60 b0 28 76 be 8d a6   .z..h|L..`.(v...
    0040 - 27 db 15 8b 1d 6d d6 1f-0f 65 6c a6 01 7a 86 92   '....m...el..z..
    0050 - f2 96 2e ed 6f b4 ab 5b-31 40 0e b2 1c 2f 94 17   ....o..[1@.../..
    0060 - 6d 1a e4 a5 fb 20 0a c5-02 ba a4 11 21 ed b9 88   m.... ......!...
    0070 - e3 0a 25 ea 79 dc 87 ff-6e e8 09 2e 21 74 98 b3   ..%.y...n...!t..
    0080 - 0e 6a b4 fa f0 b4 dc 33-15 8c fe 38 18 6a 4e b5   .j.....3...8.jN.
    0090 - 5e 3c ea 82 66 97 f6 58-01 c4 ba b3 2a cd a2 48   ^<..f..X....*..H



Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----



 

**I attempted to try and understand this, but it got deep and I stopped here to focus on chapter 1 quiz** 






**Found and Used Passwords Masterlist**

Lv 0 - Bandit0

Lv 1 - boJ9jbbUNNfktd78OOpsqOltutMc3MY1

Lv 2 - CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

Lv 3 - UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

Lv 4- pIwrPrtPN36QITSp3EQaw936yaFoFgAB

Lv 5- koReBOKuIDDepwhWk7jZC0RTdopnAYKh

Lv 6  - DXjZPULLxYr17uwoI01bNLQbtFemEgo7

Lv 7 - HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

Lv 8- cvX2JJa4CFALtqS87jk27qwqGhBM9plV

Lv 9 - UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

Lv 10 - truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

LV 11 - IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

Lv 12 - 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

lv 13 - 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

Lv 14 - 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

Lv 15 - BfMYroe26WYalil77FoDi9qh59eK5xNr

Lv 16- cluFn7wTiGryunymYOu4RcffSxQluehd
