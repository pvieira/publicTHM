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

![](../.gitbook/assets/image%20%28428%29.png)

{% hint style="success" %}
3
{% endhint %}

### How you redirect yourself to a secret page?

![](../.gitbook/assets/image%20%28417%29.png)

> Switch User-Agent to C

![](../.gitbook/assets/image%20%28388%29.png)

{% hint style="success" %}
User-Agent
{% endhint %}

### What is the agent name?

{% hint style="success" %}
Chris
{% endhint %}

## Task 3 Hash cracking and brute-force

### FTP password 

### Zip file password 

### steg password 

### Who is the other agent \(in full name\)? 

### SSH password

## Task 4 Capture the user flag



## Task 5 Privilege escalation



