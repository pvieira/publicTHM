# Hashing - Crypto 101

## Task 1 Key Terms

Before we start, we need to get some jargon out of the way. Read these, and take in as much as you can. We'll expand on some of them later in the room.

**Plaintext -** Data before encryption or hashing, often text but not always as it could be a photograph or other file instead.

**Encoding -** This is NOT a form of encryption, just a form of data representation like base64 or hexadecimal. Immediately reversible.

**Hash -** A hash is the output of a hash function. Hashing can also be used as a verb, "to hash", meaning to produce the hash value of some data.

**Brute force -** Attacking cryptography by trying every different password or every different key

**Cryptanalysis -** Attacking cryptography by finding a weakness in the underlying maths This room will likely involve some research. Get good at using search engines, it's crucial to infosec.

### Read the words, and understand the meanings! Is base64 encryption or encoding?

{% hint style="success" %}
encoding
{% endhint %}

## Task 2 What is a hash function?

### What is the output size in bytes of the MD5 hash function?

128 bit= 16 bytes

{% hint style="success" %}
16
{% endhint %}

### Can you avoid hash collisions? \(Yea/Nay\)

{% hint style="success" %}
Nay
{% endhint %}

### If you have an 8 bit hash output, how many possible hashes are there?

2⁸=256

{% hint style="success" %}
256
{% endhint %}

## Task 3 Uses for hashing

### Crack the hash "d0199f51d2728db6011945145a1b607a" using the rainbow table manually.

{% hint style="success" %}
basketball
{% endhint %}

### Crack the hash "5b31f93c09ad1d065c0491b764d04933" using online tools

{% embed url="https://md5hashing.net/hash/md5/5b31f93c09ad1d065c0491b764d04933" %}



![](../.gitbook/assets/image%20%28294%29.png)

{% hint style="success" %}
tryhackme
{% endhint %}

### Should you encrypt passwords? Yea/Nay

{% hint style="success" %}
Nay
{% endhint %}

## Task 4 Recognising password hashes

Automated hash recognition tools such as [https://pypi.org/project/hashID/](https://pypi.org/project/hashID/)

A great place to find more hash formats and password prefixes is the hashcat example page, available here: [https://hashcat.net/wiki/doku.php?id=example\_hashes](https://hashcat.net/wiki/doku.php?id=example_hashes).

### How many rounds does sha512crypt \($6$\) use by default?

{% hint style="success" %}
5000
{% endhint %}

### What's the hashcat example hash \(from the website\) for Citrix Netscaler hashes?



{% hint style="success" %}
5000
{% endhint %}

### How long is a Windows NTLM hash, in characters?



{% hint style="success" %}
5000
{% endhint %}

## Task 5 Password Cracking



## Task 6 Hashing for integrity checking

### What's the SHA1 sum for the amd64 Kali 2019.4 ISO? [http://old.kali.org/kali-images/kali-2019.4/](http://old.kali.org/kali-images/kali-2019.4/)

![](../.gitbook/assets/image%20%28316%29.png)

{% hint style="success" %}
186c5227e24ceb60deb711f1bdc34ad9f4718ff9
{% endhint %}

### What's the hashcat mode number for HMAC-SHA512 \(key = $pass\)?

{% embed url="https://hashcat.net/wiki/doku.php?id=example\_hashes" %}

![](../.gitbook/assets/image%20%28315%29.png)

{% hint style="success" %}
1750
{% endhint %}

