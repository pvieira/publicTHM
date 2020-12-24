---
description: Web
---

# The Trial Before Christmas

## Video

## Resources

## Challenges

### Scan the machine. What ports are open?

```text
nmap -sC -sV -T5 -p1-65535 10.10.243.219
```

![](../.gitbook/assets/image%20%28362%29.png)

{% hint style="success" %}
80, 65000
{% endhint %}

### What's the title of the hidden website? It's worthwhile looking recursively at all websites on the box for this step.

```text
gobuster dir -u http://10.10.243.219 -w /usr/share/dirb/wordlists/common.txt
```

![](../.gitbook/assets/image%20%28364%29.png)

```text
gobuster dir -u http://10.10.243.219:65000 -w /usr/share/dirb/wordlists/common.txt -x php -t 50
```

![](../.gitbook/assets/image%20%28361%29.png)

![](../.gitbook/assets/image%20%28359%29.png)

{% hint style="success" %}
Light Cycle
{% endhint %}

### What is the name of the hidden php page?

```text
gobuster dir -u http://10.10.243.219:65000 -w /usr/share/dirb/wordlists/common.txt -x php -t 50
```

![](../.gitbook/assets/image%20%28360%29.png)

{% hint style="success" %}
uploads.php
{% endhint %}

### What is the name of the hidden directory where file uploads are saved?

{% hint style="success" %}
grid
{% endhint %}

### Bypass the filters. Upload and execute a reverse shell. 

{% hint style="success" %}

{% endhint %}

What is the value of the web.txt flag?



Upgrade and stabilize your shell.



Review the configuration files for the webserver to find some useful loot in the form of credentials. What credentials do you find? **username:password**

\*\*\*\*

Access the database and discover the encrypted credentials. What is the name of the database you find these in?



Crack the password. What is it?



Use su to login to the newly discovered user by exploiting password reuse.



What is the value of the user.txt flag?



### Check the user's groups. Which group can be leveraged to escalate privileges?

###  

### Abuse this group to escalate privileges to root.



### What is the value of the root.txt flag?



