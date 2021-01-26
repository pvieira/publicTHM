---
description: 'https://tryhackme.com/room/agentsudoctf'
---

# Agent Sudo

## INIT

```text
export agentsudo=10.10.172.140
ping $agentsudo

echo "10.10.172.140 agentsudo.thm" >> /etc/hosts
```

## Task 2 Enumerate

```text
nmap -v -sC -sV -O -T5 -p1-65535 agentsudo.thm
```

### How many open ports?

![](../.gitbook/assets/image%20%28433%29.png)

{% hint style="success" %}
3
{% endhint %}

### How you redirect yourself to a secret page?

![](../.gitbook/assets/image%20%28422%29.png)

> Switch User-Agent to C

![](../.gitbook/assets/image%20%28391%29.png)

{% hint style="success" %}
User-Agent
{% endhint %}

### What is the agent name?

{% hint style="success" %}
Chris
{% endhint %}

## Task 3 Hash cracking and brute-force

### FTP password

```text
hydra -l chris -P /usr/share/wordlists/rockyou.txt ftp://agentsudo.thm -t 50
```

![](../.gitbook/assets/image%20%28394%29.png)

{% hint style="success" %}
crystal
{% endhint %}

### Zip file password 

![](../.gitbook/assets/image%20%28384%29.png)

```text
binwalk -e cutie.png

zip2john 8702.zip > ziphash.txt
john ziphash.txt --wordlist=/usr/share/wordlists/rockyou.txt
```

![](../.gitbook/assets/image%20%28380%29.png)

{% hint style="success" %}
alien
{% endhint %}

### steg password 

![](../.gitbook/assets/image%20%28408%29.png)

{% hint style="success" %}
Area51
{% endhint %}

### Who is the other agent \(in full name\)? 

{% hint style="success" %}
james
{% endhint %}

### SSH password

{% hint style="success" %}
hackerrules
{% endhint %}

## Task 4 Capture the user flag



## Task 5 Privilege escalation



