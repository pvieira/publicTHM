---
description: 'https://tryhackme.com/room/linuxctf'
---

# LinuxCTF - Linux Challenges - wip

ssh 10.10.255.137 Username: garry Password: letmein

**\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#**

shell5@x240:~/hack/thm/Linux\_Challenges$ ssh garry@10.10.255.137 The authenticity of host '10.10.255.137 \(10.10.255.137\)' can't be established. ECDSA key fingerprint is SHA256:gEjuE22rM5GVDKW9+IAOHT1vKNqL5vDSLmZ/o7Q29PM. Are you sure you want to continue connecting \(yes/no\)? yes Warning: Permanently added '10.10.255.137' \(ECDSA\) to the list of known hosts. garry@10.10.255.137's password: Last login: Fri Nov 22 22:21:47 2019 from 10.10.231.194

**\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#**

## Task 1 Linux Challenges Introduction

### 1 How many visible files can you see in garrys home directory?

garry@ip-10-10-255-137:~$ ls flag1.txt flag24 flag29 garry@ip-10-10-255-137:~$ ls \| wc -l 3

{% hint style="success" %}

{% endhint %}

## Task 2 The Basics

### 1 What is flag 1?

garry@ip-10-10-255-137:~$ cat flag1.txt There are flags hidden around the file system, its your job to find them.

Flag 1: f40dc0cff080ad38a6ba9a1c2c038b2c

Log into bobs account to get flag 2.

Username: bob Password: linuxrules

{% hint style="success" %}

{% endhint %}

### 2    Log into bob's account using the credentials shown in flag 1.

What is flag 2?

garry@ip-10-10-255-137:~$ ssh bob@localhost The authenticity of host 'localhost \(127.0.0.1\)' can't be established. ECDSA key fingerprint is SHA256:gEjuE22rM5GVDKW9+IAOHT1vKNqL5vDSLmZ/o7Q29PM. Are you sure you want to continue connecting \(yes/no\)? yes Warning: Permanently added 'localhost' \(ECDSA\) to the list of known hosts. bob@localhost's password: Permission denied, please try again. bob@localhost's password:

The programs included with the Ubuntu system are free software; the exact distribution terms for each program are described in the individual files in /usr/share/doc/\*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by applicable law.

bob@ip-10-10-255-137:~$ cat flag2.txt Flag 2: 8e255dfa51c9cce67420d2386cede596

{% hint style="success" %}

{% endhint %}

### 3 Flag 3 is located where bob's bash history gets stored.

bob@ip-10-10-255-137:~$ cat .bash\_history 9daf3281745c2d75fc6e992ccfdedfcd

{% hint style="success" %}

{% endhint %}

### 4 Flag 4 is located where cron jobs are created.

bob@ip-10-10-255-137:~$ crontab -e

Edit this file to introduce tasks to be run by cron.

Each task to run has to be defined through a single line

indicating with different fields when the task will be run

and what command to run for the task

To define the time you can provide concrete values for

minute \(m\), hour \(h\), day of month \(dom\), month \(mon\),

and day of week \(dow\) or use '\*' in these fields \(for 'any'\).\#

Notice that tasks will be started based on the cron's system

daemon's notion of time and timezones.

Output of the crontab jobs \(including errors\) is sent through

email to the user the crontab file belongs to \(unless redirected\).

For example, you can run a backup of all your user accounts

at 5 a.m every week with:

0 5  __ 1 tar -zcf /var/backups/home.tgz /home/

For more information see the manual pages of crontab\(5\) and cron\(8\)

m h  dom mon dow   command

0 6  __ \* echo 'flag4:dcd5d1dcfac0578c99b7e7a6437827f3' &gt; /home/bob/flag4.txt

{% hint style="success" %}

{% endhint %}

### 5 Find and retrieve flag 5.

bob@ip-10-10-255-137:~$ cat $\(locate flag5.txt\) bd8f33216075e5ba07c9ed41261d1703

{% hint style="success" %}

{% endhint %}

### 6 "Grep" through flag 6 and find the flag. The first 2 characters of the flag is c9.

bob@ip-10-10-177-45:~$ grep 'c9' $\(locate flag6.txt\) Sed sollicitudin eros quis vulputate rutrum. Curabitur mauris elit, elementum quis sapien sed, ullamcorper pellentesque neque. Aliquam erat volutpat. Cras vehicula mauris vel lectus hendrerit, sed malesuada ipsum consectetur. Donec in enim id erat condimentum vestibulum c9e142a1e25b24a837b98db589b08be5 vitae eget nisi. Suspendisse eget commodo libero. Mauris eget gravida quam, a interdum orci. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Quisque eu nisi non ligula tempor efficitur. Etiam eleifend, odio vel bibendum mattis, purus metus consectetur turpis, eu dignissim elit nunc at tortor. Mauris sapien enim, elementum faucibus magna at, rutrum venenatis ipsum.

bob@ip-10-10-177-45:~$ grep -o '\w{32}' $\(locate flag6.txt\) c9e142a1e25b24a837b98db589b08be5

bob@ip-10-10-177-45:~$ sed -n "/c9/,/ /p" ../flag6.txt Sed sollicitudin eros quis vulputate rutrum. Curabitur mauris elit, elementum quis sapien sed, ullamcorper pellentesque neque. Aliquam erat volutpat. Cras vehicula mauris vel lectus hendrerit, sed malesuada ipsum consectetur. Donec in enim id erat condimentum vestibulum c9e142a1e25b24a837b98db589b08be5 vitae eget nisi. Suspendisse eget commodo libero. Mauris eget gravida quam, a interdum orci. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Quisque eu nisi non ligula tempor efficitur. Etiam eleifend, odio vel bibendum mattis, purus metus consectetur turpis, eu dignissim elit nunc at tortor. Mauris sapien enim, elementum faucibus magna at, rutrum venenatis ipsum.

{% hint style="success" %}

{% endhint %}

### 7 Look at the systems processes. What is flag 7.

bob@ip-10-10-99-145:~$ ps -aef \|grep flag root 1391 1 0 09:23 ? 00:00:00 flag7:274adb75b337307bd57807c005ee6358 1000000 bob 2099 2081 0 09:26 pts/2 00:00:00 grep --color=auto flag

{% hint style="success" %}

{% endhint %}

bob@ip-10-10-99-145:~$ dir Desktop Downloads Pictures Templates flag13 flag21.php Documents Music Public Videos flag2.txt flag8.tar.gz bob@ip-10-10-99-145:~$ tar -xvzf flag8.tar.gz flag8.txt bob@ip-10-10-99-145:~$ cat flag8.txt 75f5edb76fe98dd5fc9f577a3f5de9bc

{% hint style="success" %}

{% endhint %}

## 9 By look in your hosts file, locate and retrieve flag 9.

bob@ip-10-10-99-145:~$ tail -n 1 /etc/hosts 127.0.0.1 dcf50ad844f9fe06339041ccc0d6e280.com

{% hint style="success" %}

{% endhint %}

### 10 Find all other users on the system. What is flag 10.

bob@ip-10-10-99-145:~$ cat /etc/passwd root:x:0:0:root:/root:/bin/bash 5e23deecfe3a7292970ee48ff1b6d00c:x:1002:1002:,,,:/home/5e23deecfe3a7292970ee48ff1b6d00c:/bin/bash

{% hint style="success" %}

{% endhint %}

## Task 3 Linux Functionality

### 1 Run the command flag11. Locate where your command alias are stored and get flag 11.

bob@ip-10-10-99-145:~$ cat .bashrc \|grep flag11 alias flag11='echo "You need to look where the alias are created..."' \#b4ba05d85801f62c4c0d05d3a76432e0

{% hint style="success" %}

{% endhint %}

### 2 Flag12 is located were MOTD's are usually found on an Ubuntu OS. What is flag12?

bob@ip-10-10-99-145:~$ cat /etc/update-motd.d/00-header \|grep Flag12

Flag12: 01687f0c5e63382f1c9cc783ad44ff7f

{% hint style="success" %}

{% endhint %}

### 3 Find the difference between two script files to find flag 13.

bob@ip-10-10-99-145:~$ cd flag13/ bob@ip-10-10-99-145:~/flag13$ dir script1 script2 bob@ip-10-10-99-145:~/flag13$ diff script1 script2 2437c2437

> Lightoller sees 3383f3771ba86b1ed9ab7fbf8abab531 Smith walking stiffly toward him and quickly goes to him. He yells into the Captain's ear, through cupped hands, over the roar of the steam...

{% hint style="success" %}

{% endhint %}

### 4 Where on the file system are logs typically stored? Find flag 14.

bob@ip-10-10-99-145:~/flag13$ tail -n 1 /var/log/flagtourteen.txt 71c3a8ad9752666275dadf62a93ef393

{% hint style="success" %}

{% endhint %}

### 5 Can you find information about the system, such as the kernel version etc.

Find flag 15.

bob@ip-10-10-99-145:~/flag13$ ls /etc/ \|grep release lsb-release os-release bob@ip-10-10-99-145:~/flag13$ cat /etc/lsb-release FLAG\_15=a914945a4b2b5e934ae06ad6f9c6be45

{% hint style="success" %}

{% endhint %}

### 6 Flag 16 lies within another system mount.

bob@ip-10-10-99-145:~$ cd /media/f/l/a/g/1/6/is/cab4b7cae33c87794d82efa1e7f834e6/ bob@ip-10-10-99-145:/media/f/l/a/g/1/6/is/cab4b7cae33c87794d82efa1e7f834e6$

{% hint style="success" %}

{% endhint %}

### 7 Login to alice's account using her private key and get flag 17.

bob@ip-10-10-99-145:~$ ssh alice@localhost alice@localhost's password: Last login: Sat Nov 23 09:40:22 2019 from 127.0.0.1 -bash: warning: setlocale: LC\_CTYPE: cannot change locale \(pt\_PT.UTF-8\) alice@ip-10-10-99-145:~$ cat flag17 89d7bce9d0bab49e11e194b54a601362

{% hint style="success" %}

{% endhint %}

### 8 Find the hidden flag 18.

alice@ip-10-10-99-145:~$ cat .flag18 c6522bb26600d30254549b6574d2cef2

{% hint style="success" %}

{% endhint %}

### 9 Read the 2345th line of the file that contains flag 19.

alice@ip-10-10-99-145:~$ awk 'NR==2345' flag19 490e69bd1bf3fc736cce9ff300653a3b

alice@ip-10-10-99-145:~$ sed '2345!d' flag19 490e69bd1bf3fc736cce9ff300653a3b

{% hint style="success" %}

{% endhint %}

## Task 4 Data Representation, Strings and Permissions

### 1 Find and retrieve flag 20.

alice@ip-10-10-71-95:~$ locate flag20 /home/alice/flag20 alice@ip-10-10-71-95:~$ cat $\(locate flag20\) MDJiOWFhYjhhMjk5NzBkYjA4ZWM3N2FlNDI1ZjZlNjg= alice@ip-10-10-71-95:~$ cat $\(locate flag20\) \|base64 -d 02b9aab8a29970db08ec77ae425f6e68

{% hint style="success" %}

{% endhint %}

### 2 Inspect the flag21.php file. Find the flag.

alice@ip-10-10-71-95:~$ locate flag21.php /home/bob/flag21.php

alice@ip-10-10-71-95:~$ less /home/bob/flag21.php &lt;?=`$_POST[flag21_g00djob]`?&gt;^M&lt;?='MoreToThisFileThanYouThink';?&gt;

{% hint style="success" %}

{% endhint %}

### 3 Locate and read flag 22. Its represented as hex.

alice@ip-10-10-71-95:~$ cat flag22 \|xxd -r -p 9d1ae8d569c83e03d8a8f61568a0fa7d

{% hint style="success" %}

{% endhint %}

### 4 Locate, read and reverse flag 23.

alice@ip-10-10-71-95:~$ cat $\(locate flag23\) \|rev ea52970566f4c090a7348b033852bff5

{% hint style="success" %}

{% endhint %}

### 5 Analyse the flag 24 compiled C program. Find a command that might reveal human readable strings when looking in the source code.

alice@ip-10-10-71-95:~$ strings $\(locate flag24\) \|grep flag flag24.c flag\_24\_is\_hidd3nStr1ng

{% hint style="success" %}

{% endhint %}

### 7 Locate and retrieve flag 26.

alice@ip-10-10-71-95:~$ cat /var/cache/apache2/mod\_cache\_disk/config.json flag twenty6

4bceb76f490b24ed577d704c24d6955d

{% hint style="success" %}

{% endhint %}

### 8 Locate and retrieve flag 27, which is owned by the root user.

alice@ip-10-10-71-95:~$ locate flag27 /home/flag27 alice@ip-10-10-71-95:~$ ls -lah /home/ total 296K drwxr-xr-x 6 root root 4.0K Feb 20 2019 . drwxr-xr-x 23 root root 4.0K Nov 23 15:10 .. drwxr-xr-x 4 alice alice 4.0K Nov 23 15:17 alice drwxr-xr-x 21 bob bob 4.0K Feb 20 2019 bob -rwx------ 1 root root 33 Feb 19 2019 flag27 -rwxr-xr-x 1 root root 266K Feb 18 2019 flag6.txt drwxr-xr-x 3 garry garry 4.0K Feb 20 2019 garry drwxr-xr-x 19 ubuntu ubuntu 4.0K Mar 7 2019 ubuntu alice@ip-10-10-71-95:~$ sudo cat /home/flag27 6fc0c805702baebb0ecc01ae9e5a0db5

{% hint style="success" %}

{% endhint %}

### Whats the linux kernel version?

```text
alice@ip-10-10-71-95:~$ uname -r
4.4.0-1075-aws
```

{% hint style="success" %}
4.4.0-1075-aws
{% endhint %}

### Find the file called flag 29 and do the following operations on it:

Remove all spaces in file. Remove all new line spaces. Split by comma and get the last element in the split.

```text
alice@ip-10-10-71-95:~$ cat $(locate flag29) | tr -d ' ' | tr -d '\n' |awk -F',' '{print $NF}'
fastidiisuscipitmeaei
alice@ip-10-10-71-95:~$ cat $(locate flag29) | tr -d ' ' | tr -d '\n' |awk -F',' '{print $NF}' |grep -E "[0-9a-z]"
```

{% hint style="success" %}
fastidiisuscipitmeaei
{% endhint %}

## Task 5 SQL, FTP, Groups and RDP

### Use curl to find flag 30.

```text
alice@ip-10-10-71-95:~$ curl localhost
flag30:fe74bb12fe03c5d8dfc245bdd1eae13f
```

{% hint style="success" %}
fe74bb12fe03c5d8dfc245bdd1eae13f
{% endhint %}

### Flag 31 is a MySQL database name.

> MySQL username: root
>
> MySQL password: hello

```text
alice@ip-10-10-71-95:~$ mysql -u root -p 
Enter password:
Welcome to the MySQL monitor.
Commands end with ; or \g.
Your MySQL connection id is 6 Server version: 5.7.25-0ubuntu0.16.04.2 (Ubuntu)
Copyright (c) 2000, 2019, Oracle and/or its affiliates. All rights reserved.
Oracle is a registered trademark of Oracle Corporation and/or its affiliates.
Other names may be trademarks of their respective owners.
Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
mysql> show databases;
+-------------------------------------------+
| Database |
+-------------------------------------------+
| information_schema |
| database_2fb1cab13bf5f4d61de3555430c917f4 |
| mysql |
| performance_schema |
| sys |
+-------------------------------------------+
5 rows in set (0.00 sec)
```

{% hint style="success" %}
2fb1cab13bf5f4d61de3555430c917f4
{% endhint %}

### Bonus flag question, get data out of the table from the database you found above!

```text
mysql> use database_2fb1cab13bf5f4d61de3555430c917f4 
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed mysql> show tables; 
+-----------------------------------------------------+ 
| Tables_in_database_2fb1cab13bf5f4d61de3555430c917f4 |
+-----------------------------------------------------+
| flags |
+-----------------------------------------------------+
1 row in set (0.00 sec)

mysql> select * from flags; 
+----+----------------------------------+
| id | flag | +----+----------------------------------+
| 1 | ee5954ee1d4d94d61c2f823d7b9d733c |
+----+----------------------------------+
1 row in set (0.00 sec)
```

{% hint style="success" %}
ee5954ee1d4d94d61c2f823d7b9d733c
{% endhint %}

### Using SCP, FileZilla or another FTP client download flag32.mp3 to reveal flag 32.

```text
scp alice@10.10.71.95:flag32.mp3 . 
alice@10.10.71.95's password: 
flag32.mp3 100% 10KB 196.7KB/s 00:00
audacity flag32.mp3
```

{% hint style="success" %}
tryhackme1337
{% endhint %}

### Flag 33 is located where your personal $PATH's are stored.

```text
bob@ip-10-10-71-95:~$ head -n 1 .profile
Flag 33: 547b6ceee3c5b997b625de99b044f5cf
```

{% hint style="success" %}
547b6ceee3c5b997b625de99b044f5cf
{% endhint %}

### Switch your account back to bob. Using system variables, what is flag34?

```text
bob@ip-10-10-71-95:~$ printenv |grep flag 
flag34=7a88306309fe05070a7c5bb26a6b2def
```

{% hint style="success" %}
7a88306309fe05070a7c5bb26a6b2def
{% endhint %}

### Look at all groups created on the system. What is flag 35?

```text
bob@ip-10-10-71-95:~$ cat /etc/group |grep flag
flag35_769afb6:x:1005:
bob@ip-10-10-71-95:~$ getent group |grep flag
flag35_769afb6:x:1005:
```

{% hint style="success" %}
769afb6
{% endhint %}

### Find the user which is apart of the "hacker" group and read flag 36.

```text
bob@ip-10-10-71-95:~$ locate flag36 /etc/flag36
bob@ip-10-10-71-95:~$ ls -lah /etc/flag36
-rw-r----- 1 root hacker 33 Feb 19 2019 /etc/flag36 
bob@ip-10-10-71-95:~$ cat /etc/group |grep hacker hacker:x:1004:bob 
bob@ip-10-10-71-95:~$ cat /etc/flag36 
83d233f2ffa388e5f0b053848caed1eb
```

{% hint style="success" %}
83d233f2ffa388e5f0b053848caed1eb
{% endhint %}

### Well done! You've completed the LinuxCTF room!

{% hint style="success" %}
No answer needed
{% endhint %}

