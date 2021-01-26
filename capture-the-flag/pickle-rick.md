---
description: 'https://tryhackme.com/room/picklerick'
---

# Pickle Rick

## INIT

```text
export pickle=10.10.173.224
ping $pickle

echo "10.10.173.224 pickle.thm" >> /etc/hosts
```

## NMAP

```text
nmap -v -sC -sV -O -T5 -p1-65535 pickle.thm
```

![](../.gitbook/assets/image%20%28414%29.png)

## HTTP

![](../.gitbook/assets/image%20%28382%29.png)

![](../.gitbook/assets/image%20%28386%29.png)

{% hint style="info" %}
Username: R1ckRul3s
{% endhint %}

![](../.gitbook/assets/image%20%28426%29.png)

{% hint style="info" %}
Wubbalubbadubdub
{% endhint %}

## GOBUSTER

```text
gobuster dir -u pickle.thm -w /usr/share/wordlists/dirb/common.txt -q -t 15 -x php,html,txt
```

![](../.gitbook/assets/image%20%28416%29.png)

## Login

{% hint style="info" %}
Username: R1ckRul3s

Password: Wubbalubbadubdub
{% endhint %}

![](../.gitbook/assets/image%20%28407%29.png)

![](../.gitbook/assets/image%20%28392%29.png)

## What is the first ingredient Rick needs?

![](../.gitbook/assets/image%20%28415%29.png)

![](../.gitbook/assets/image%20%28378%29.png)

{% hint style="success" %}
mr. meeseek hair
{% endhint %}

## Whats the second ingredient Rick needs?

![](../.gitbook/assets/image%20%28384%29.png)

![](../.gitbook/assets/image%20%28424%29.png)

{% hint style="success" %}
1 jerry tear
{% endhint %}

## Whats the final ingredient Rick needs?

![](../.gitbook/assets/image%20%28383%29.png)

![](../.gitbook/assets/image%20%28410%29.png)

![](../.gitbook/assets/image%20%28398%29.png)

{% hint style="success" %}
fleeb juice
{% endhint %}

