---
description: 'https://tryhackme.com/room/linux3'
---

# Linux Fundamentals Part 3 - wip

## Task 1 Intro

### Read the above.

{% hint style="success" %}
No answer needed
{% endhint %}

### Deploy the machine attached to this task!

{% hint style="success" %}
No answer needed
{% endhint %}

## Task 2 \[Section 5: Advanced File Operations\] - cp

cp duplicates\(copies\) files. The syntax is  `cp <file> <destination>` 

{% hint style="success" %}
No answer needed
{% endhint %}

## Task 3 \[Section 5: Advanced file Operations\] - cd && mkdir

Linux allows you to change the location of the current directory through the use of the cd command. The syntax of the cd command is this, `cd <directory>`.

This brings us to mkdir, occasionally you'll want to make a new directory to store files in, and that is done using mkdir, the syntax of mkdir is `mkdir <directory name>`.

###  Using relative paths, how would you cd to your home directory.

{% hint style="success" %}
cd ~
{% endhint %}

### Using absolute paths how would you make a directory called test in /tmp

{% hint style="success" %}
mkdir /tmp/test
{% endhint %}

## Task 4 \[Section 5: Advanced File Operations\] ln

The ln syntax is `ln source destination`.

The syntax for a symbolic link is the exact same, but it uses the -s flag, so to create a symbolic link, you would run `ln -s <file> <destination>`.

### How would I link /home/test/testfile to /tmp/test

{% hint style="success" %}
ln /home/test/testfile /tmp/test
{% endhint %}

## Task 5 \[Section 5 - Advanced File Operations\]: find

The true power of this command though comes from the parameters you can provide it. You can use `find dir -user` , to list every file owned by a specific user; you can use `find dir -group` to list every file owned by a specific group.

### How do you find files that have specific permissions?

{% hint style="success" %}
-perm
{% endhint %}

### How would you find all the files in /home

{% hint style="success" %}
find /home
{% endhint %}

### How would you find all the files owned by paradox on the whole system

{% hint style="success" %}
find / -user paradox
{% endhint %}

## Task 6 \[Section 5: Advanced File Operations\] - grep

`grep <regular expression> <file>`

### What flag lists line numbers for every string found?

{% hint style="success" %}
-n
{% endhint %}

### How would I search for the string boop in the file aaaa in the directory /tmp

{% hint style="success" %}
grep boop /tmp/aaaa
{% endhint %}

## Task 7 Binary - Shiba3

### What is shiba4's password

{% hint style="success" %}
test1234
{% endhint %}

## Task 8 \[Section 6: Miscellaneous\]: Intro



## Task 9 \[Section 6: Miscellaneous\]: sudo



## Task 10 \[Section 6: Miscellaneous\]: Adding users and groups



## Task 11 \[Section 6: Miscellaneous\]: nano



## Task 12 \[Section 6: Miscellaneous\]: Basic shell scripting



## Task 13 \[Section 6: Miscellaneous\]: Important Files and Directories



## Task 14 \[Section 6 - Miscellaneous\]: Installing packages\(apt\)



## Task 15 \[Section 6: Miscellaneous\]: Processes



