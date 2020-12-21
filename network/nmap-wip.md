---
description: 'https://tryhackme.com/room/furthernmap'
---

# Nmap - wip

## Task 1 Deploy

Deploy the attached VM

{% hint style="success" %}
No answer needed
{% endhint %}

## Task 2 Introduction

Every computer has a total of 65535 available ports;

### What networking constructs are used to direct traffic to the right application on a server?

{% hint style="success" %}
Ports
{% endhint %}

### How many of these are available on any network-enabled computer?

{% hint style="success" %}
65535
{% endhint %}

### **\[Research\]** How many of these are considered "well-known"? \(These are the "standard" numbers mentioned in the task\)

{% hint style="success" %}
1024
{% endhint %}

## Task 3 Nmap Switches

### What is the first switch listed in the help menu for a 'Syn Scan' \(more on this later!\)?

{% hint style="success" %}
-sS
{% endhint %}

### Which switch would you use for a "UDP scan"?

{% hint style="success" %}
-sU
{% endhint %}

### If you wanted to detect which operating system the target is running on, which switch would you use?

{% hint style="success" %}
-O
{% endhint %}

### Nmap provides a switch to detect the version of the services running on the target. What is this switch?

{% hint style="success" %}
-sV
{% endhint %}

### The default output provided by nmap often does not provide enough information for a pentester. How would you increase the verbosity?

{% hint style="success" %}
-v
{% endhint %}

### Verbosity level one is good, but verbosity level two is better! How would you set the verbosity level to two?  \(**Note**: it's highly advisable to always use _at least_ this option\)

{% hint style="success" %}
-vv
{% endhint %}

### We should always save the output of our scans -- this means that we only need to run the scan once \(reducing network traffic and thus chance of detection\), and gives us a reference to use when writing reports for clients.

### What switch would you use to save the nmap results in three major formats?

{% hint style="success" %}
-oA
{% endhint %}

### What switch would you use to save the nmap results in a "normal" format?

{% hint style="success" %}
-oN
{% endhint %}

### A very useful output format: how would you save results in a "grepable" format?

{% hint style="success" %}
-oG
{% endhint %}

### Sometimes the results we're getting just aren't enough. If we don't care about how loud we are, we can enable "aggressive" mode. This is a shorthand switch that activates service detection, operating system detection, a traceroute and common script scanning.

### How would you activate this setting?

{% hint style="success" %}
-A
{% endhint %}

### Nmap offers five levels of "timing" template. These are essentially used to increase the speed your scan runs at. Be careful though: higher speeds are noisier, and can incur errors!

### How would you set the timing template to level 5?

{% hint style="success" %}
-T5
{% endhint %}

### We can also choose which port\(s\) to scan.

### How would you tell nmap to only scan port 80?

{% hint style="success" %}
-p 80
{% endhint %}

### How would you tell nmap to scan ports 1000-1500?

{% hint style="success" %}
-p 1000-1500
{% endhint %}

### A very useful option that should not be ignored:

### How would you tell nmap to scan _all_ ports?

{% hint style="success" %}
-p-
{% endhint %}

### How would you activate a script from the nmap scripting library \(lots more on this later!\)?

{% hint style="success" %}
--script
{% endhint %}

### How would you activate all of the scripts in the "vuln" category?

{% hint style="success" %}
--script=vuln
{% endhint %}

## Task 4 \[Scan Types\] Overview

When port scanning with Nmap, there are three basic scan types. These are:

* TCP Connect Scans \(`-sT`\)
* SYN "Half-open" Scans \(`-sS`\)
* UDP Scans \(`-sU`\)

Additionally there are several less common port scan types, some of which we will also cover \(albeit in less detail\). These are:

* TCP Null Scans \(`-sN`\)
* TCP FIN Scans \(`-sF`\)
* TCP Xmas Scans \(`-sX`\)

Read the Scan Types Introduction.

{% hint style="success" %}
No answer needed
{% endhint %}

## Task 5 \[Scan Types\] TCP Connect Scans

To understand TCP Connect scans \(`-sT`\), it's important that you're comfortable with the _TCP three-way handshake_.

![](../.gitbook/assets/image%20%28245%29.png)

Many firewalls are configured to simply **drop** incoming packets. For example, in IPtables for Linux, a simple version of the command would be as follows:

`iptables -I INPUT -p tcp --dport <port> -j REJECT --reject-with tcp-reset`

### Which RFC defines the appropriate behaviour for the TCP protocol?

{% hint style="success" %}
RFC 793
{% endhint %}

### If a port is closed, which flag should the server send back to indicate this?

{% hint style="success" %}
RST
{% endhint %}

## Task 6 \[Scan Types\] SYN Scans

As with TCP scans, SYN scans \(`-sS`\) are used to scan the TCP port-range of a target or targets; however, the two scan types work slightly differently. SYN scans are sometimes referred to as "Half-open" scans, or "Stealth" scans.

![](../.gitbook/assets/image%20%28244%29.png)

This has a variety of advantages for us as hackers:

* It can be used to bypass older Intrusion Detection systems as they are looking out for a full three way handshake. This is often no longer the case with modern IDS solutions; it is for this reason that SYN scans are still frequently referred to as "stealth" scans.
* SYN scans are often not logged by applications listening on open ports, as standard practice is to log a connection once it's been fully established. Again, this plays into the idea of SYN scans being stealthy.
* Without having to bother about completing \(and disconnecting from\) a three-way handshake for every port, SYN scans are significantly faster than a standard TCP Connect scan.

There are, however, a couple of disadvantages to SYN scans, namely:

* They require sudo permissions\[1\] in order to work correctly in Linux. This is because SYN scans require the ability to create raw packets \(as opposed to the full TCP handshake\), which is a privilege only the root user has by default.
* Unstable services are sometimes brought down by SYN scans, which could prove problematic if a client has provided a production environment for the test.

###  There are two other names for a SYN scan, what are they?

{% hint style="success" %}
Half-Open, Stealth
{% endhint %}

### Can Nmap use a SYN scan without Sudo permissions \(Y/N\)?

{% hint style="success" %}
N
{% endhint %}

## Task 7 \[Scan Types\] UDP Scans

Unlike TCP, UDP connections are stateless. This means that, rather than initiating a connection with a back-and-forth "handshake", UDP connections rely on sending packets to a target port and essentially hoping that they make it. This makes UDP superb for connections which rely on speed over quality \(e.g. video sharing\), but the lack of acknowledgement makes UDP significantly more difficult \(and much slower\) to scan. The switch for an Nmap UDP scan is \(`-sU`\)

When a packet is sent to an open UDP port, there should be no response. When this happens, Nmap refers to the port as being `open|filtered`. In other words, it suspects that the port is open, but it could be firewalled. If it gets a UDP response \(which is very unusual\), then the port is marked as open. More commonly there is no response, in which case the request is sent a second time as a double-check. If there is still no response then the port is marked open\|filtered and Nmap moves on.

For example, scanning with  `nmap -sU --top-ports 20 <target>`. Will scan the top 20 most commonly used UDP ports, resulting in a much more acceptable scan time

## Task 8 \[Scan Types\] NULL, FIN and Xmas

## Task 9 \[Scan Types\] ICMP Network Scanning

## Task 10 \[NSE Scripts\] Overview

## Task 11 \[NSE Scripts\] Working with the NSE

## Task 12 \[NSE Scripts\] Searching for Scripts

## Task 13 Firewall Evasion

## Task 14 Practical

## Task 15 Conclusion

