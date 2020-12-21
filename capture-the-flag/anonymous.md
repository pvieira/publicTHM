---
description: 'https://tryhackme.com/room/anonymous'
---

# anonymous

## Task 1 Pwn

### Enumerate the machine.  How many ports are open?

```text
nmap -sC -sV -T5 -p1-65535 10.10.17.122
```

![](../.gitbook/assets/image%20%28252%29.png)

{% hint style="success" %}
4
{% endhint %}

### What service is running on port 21?

![](../.gitbook/assets/image%20%28251%29.png)

{% hint style="success" %}
ftp
{% endhint %}

### What service is running on ports 139 and 445?



{% hint style="success" %}
smb
{% endhint %}

### There's a share on the user's computer.  What's it called?

{% hint style="success" %}

{% endhint %}

### user.txt 

![](../.gitbook/assets/image%20%28250%29.png)

{% hint style="success" %}

{% endhint %}

### root.txt

{% hint style="success" %}

{% endhint %}

