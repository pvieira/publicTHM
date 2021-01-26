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

![](../.gitbook/assets/image%20%28410%29.png)



## GOBUSTER

```text
gobuster dir -u mrrobot.thm -w /usr/share/wordlists/dirb/common.txt -q -t 15 -x php,html,txt
```

## HTTP

![](../.gitbook/assets/image%20%28450%29.png)

![](../.gitbook/assets/image%20%28401%29.png)

```text
wpscan --url http://mrrobot.thm --enumerate u

```

![](../.gitbook/assets/image%20%28451%29.png)

![](../.gitbook/assets/image%20%28385%29.png)

### What is key 1?

```text
curl http://mrrobot.thm/key-1-of-3.txt
```

![](../.gitbook/assets/image%20%28386%29.png)

{% hint style="success" %}
073403c8a58a1f80d943455fb30724b9
{% endhint %}

```text
curl http://mrrobot.thm/fsocity.dic --output fsocity.dic
```

![](../.gitbook/assets/image%20%28427%29.png)

