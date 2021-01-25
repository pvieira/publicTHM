---
description: 'https://tryhackme.com/room/ignite'
---

# Ignite

[https://sckull.github.io/posts/ignite/](https://sckull.github.io/posts/ignite/)

## NMAP

```text
nmap -sC -sV 10.10.99.5
```

![](../.gitbook/assets/image%20%28379%29.png)

## GOBUSTER

```text
gobuster dir -u 10.10.99.5 -w /usr/share/wordlists/dirb/common.txt -q -t 15 -x php,html,txt
```



## HTTP

![](../.gitbook/assets/image%20%28377%29.png)

![](../.gitbook/assets/image%20%28376%29.png)

![](../.gitbook/assets/image%20%28378%29.png)

