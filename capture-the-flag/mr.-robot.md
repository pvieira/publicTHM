---
description: 'https://tryhackme.com/room/mrrobot'
---

# Mr. Robot

## INIT

```text
export mrrobot=10.10.177.95
ping $mrrobot

echo "10.10.177.95 mrrobot.thm" >> /etc/hosts
```

## NMAP

```text
nmap -v -sC -sV -O -T5 -p1-65535 mrrobot.thm
```

![](../.gitbook/assets/image%20%28407%29.png)



## GOBUSTER

```text
gobuster dir -u mrrobot.thm -w /usr/share/wordlists/dirb/common.txt -q -t 15 -x php,html,txt
```

## HTTP

![](../.gitbook/assets/image%20%28446%29.png)

![](../.gitbook/assets/image%20%28398%29.png)

```text
wpscan --url http://mrrobot.thm --enumerate u
```

