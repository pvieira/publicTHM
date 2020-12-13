---
description: Networking - Samba ; smb
---

# Don't be sElfish!

## Video

{% embed url="https://www.youtube.com/watch?v=HscyCbModk4" %}

## Resources

SMB \(Server Message Block\) - Natively supported by Windows and not Linux

NFS \(Network File System\) - Natively supported by Linux and not Windows

`./enum4linux.pl -U 10.10.227.117`

`smbclient //REPLACE_INSTANCE_IP_ADDRESS/**sharename**`

## Challenge

### Using _enum4linux_, how many users are there on the Samba server \(`10.10.227.117`\)?

```text
enum4linux -U 10.10.227.117
```

![](../.gitbook/assets/image%20%2845%29.png)

{% hint style="success" %}
`3`
{% endhint %}

### Now how many "shares" are there on the Samba server?

```text
enum4linux -S 10.10.227.117
```

![](../.gitbook/assets/image%20%2860%29.png)

{% hint style="success" %}
4
{% endhint %}

### Use _smbclient_ to try to login to the shares on the Samba server \(`10.10.227.117`\). What share doesn't require a password?

```text
smbclient //10.10.227.117/tbfc-hr
smbclient //10.10.227.117/tbfc-it
smbclient //10.10.227.117/tbfc-santa
```

![](../.gitbook/assets/image%20%2882%29.png)

{% hint style="success" %}
tbfc-santa
{% endhint %}

### Log in to this share, what directory did ElfMcSkidy leave for Santa?

```text
ls
```

![](../.gitbook/assets/image%20%2842%29.png)

{% code title="note\_from\_mcskidy.txt" %}
```text
Hi Santa, I decided to put all of your favourite jingles onto this share
- allowing you access it from anywhere you like! 
Regards ~ ElfMcSkidy
```
{% endcode %}

{% hint style="success" %}
jingle-tunes
{% endhint %}

