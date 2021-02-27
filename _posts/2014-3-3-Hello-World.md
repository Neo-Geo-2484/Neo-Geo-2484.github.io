---
layout: post
title: '               CSCI -18 LAB Blog '
published: true
---


## Jeff Hepburn - Lab Blog for CSCI - 18 @ Butte College
### Instructor: Edward Miro 


### **Public Profile for THM**

[Try Hack Me Public Profile link :](https://tryhackme.com/p/neogeo2484)

https://tryhackme.com/p/neogeo2484


### **Platform Used :**

1) Kali VM on TryHackMe.com via Google Chrome 

**##  Week 5 Lab :**

### Room Blue


_Task 1-Scan and learn what exploit this machine is vulnerable to. Please note that this machine does not _respond to ping (ICMP) and may take a few minutes to boot up._

## Question 1: 
Scan the machine: 

### Commands and Process:****
apt install nmap 
nmap -Sv -SC--script vuln -oN blue.nmap 10.10.76.171

less blue.nmap - Vulnerable MS12-020 Remote Desktop Protocol Denial of service IDss: CVE, CVE: 2012-0152 -medium , 2017-03-14 -High SMBV1 


## Question 2 : 
135 , 139 and 445 are 3 ports open under 1000 so 3 ports are open.

## Question 3 : 
what is it vulnerable the High risk is ms17-010




_Task 2 Exploit the machine and gain a foothold._

## question 1:
_Start Metasploit_ 

msfconsole

## question 2:
_Find the exploitation code we will run against the machine. What is the full path of the code? (Ex: exploit/........)_

search ms17

search eternal - found that #2 matches : exploit /windows /smb/ms17_010_eternalblue 

use 2 into command 

## question 3:
Show options and set the one required value. What is the name of this value? (All caps for submission)

show options reveals the RHOSTS needs to be set_

## question 4:
U_sually it would be fine to run this exploit as is; however, for the sake of learning, you should do one more thing before exploiting the target. Enter the following command and press enter:
With that done, run the exploit!_

Task 3




Task 4 





Task 5








**##  Week 4 Lab :**



## :Link 1 Documentation:
### Room : Welcome
https://tryhackme.com/room/welcome
Room is Private - However on the Dashboard there are 3 Welcome Tasks- 
What are rooms ?
deploy machine and go to ip address in firefox
find flag 
flag{connection_verified}
check out other pathways and rooms within THM. 




## :Link 2 Documentation:
### Room : Tutorial
https://tryhackme.com/room/tutorial

Deploy My first Machine 
Open Machine Info - Copy IP and paste into Firefox 
10.10.38.0
Deploy attackbox and go to IP above to find flag
flag{connection_verified}

more next step info



## :Link 3 Documentation:
### Room : OpenVpn


Download your VPN configuration file

Run through all the different OS and how to access their VM on those OS or Run Open VPN-

Open VPN GUI download

Open and Run connect from local file 
Find Ip address and connect  then verify connection on 
Test connection by deploying machine and going to IP address listed to find the flag 

Enter flag
Flag{connection_verified}

Complete room.
