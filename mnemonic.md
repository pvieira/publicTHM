# Mnemonic

## Mnemonic

## Enumerate

### How many open ports?

```bash
nmap -sC -sV -T5 -p1-65535 10.10.109.236
```

![](.gitbook/assets/image%20%28141%29.png)

{% hint style="success" %}
3
{% endhint %}

### What is the ssh port number? 

![](.gitbook/assets/image%20%28134%29.png)

{% hint style="success" %}
1337
{% endhint %}

### What is the name of the secret file?

![](.gitbook/assets/image%20%28140%29.png)

```bash
gobuster dir -u http://10.10.109.236 -w /usr/share/dirb/wordlists/common.txt

gobuster dir -u http://10.10.109.236 -w big.txt -x php,txt,html -t 50
```

![](.gitbook/assets/image%20%28138%29.png)

```bash
gobuster dir -u http://10.10.109.236/webmasters/ -w big.txt -x php,txt,html -t 50
```

![](.gitbook/assets/image%20%28139%29.png)

```bash
gobuster dir -u http://10.10.109.236/webmasters/admin/ -w big.txt -x php,txt,html -t 50

```

![](.gitbook/assets/image%20%28133%29.png)

![](.gitbook/assets/image%20%28136%29.png)

{% hint style="success" %}
backups.zip
{% endhint %}

## Credentials

###  ftp user name? 

{% hint style="success" %}

{% endhint %}

### ftp password? 

{% hint style="success" %}

{% endhint %}

### What is the ssh username? 

{% hint style="success" %}

{% endhint %}

### What is the ssh password?

{% hint style="success" %}

{% endhint %}

### What is the condor password? 

{% hint style="success" %}

{% endhint %}

