# Encryption - Crypto 101

## What will this room cover?

{% embed url="https://tryhackme.com/room/ccpentesting" %}

I'm ready to learn about encryption

{% hint style="success" %}
No answer needed
{% endhint %}

## Key terms

**Ciphertext -** The result of encrypting a plaintext, encrypted data

**Cipher -** A method of encrypting or decrypting data. Modern ciphers are cryptographic, but there are many non cryptographic ciphers like Caesar.

**Plaintext -** Data before encryption, often text but not always. Could be a photograph or other file

**Encryption -** Transforming data into ciphertext, using a cipher.

**Encoding -** NOT a form of encryption, just a form of data representation like base64. Immediately reversible.

**Key -** Some information that is needed to correctly decrypt the ciphertext and obtain the plaintext.

**Passphrase -** Separate to the key, a passphrase is similar to a password and used to protect a key.

**Asymmetric encryption -** Uses different keys to encrypt and decrypt.

**Symmetric encryption -** Uses the same key to encrypt and decrypt

**Brute force -** Attacking cryptography by trying every different password or every different key

**Cryptanalysis -** Attacking cryptography by finding a weakness in the underlying maths

**Alice and Bob -** Used to represent 2 people who generally want to communicate. They’re named Alice and Bob because this gives them the initials A and B.

### I agree not to complain too much about how theory heavy this room is. 

{% hint style="success" %}
No answer needed
{% endhint %}

### Are SSH keys protected with a passphrase or a password?

{% hint style="success" %}
passphrase
{% endhint %}

## Why is Encryption important?

Cryptography is used to protect confidentiality, ensure integrity, ensure authenticity. You use cryptography every day most likely, and you’re almost certainly reading this now over an encrypted connection.

###  What does SSH stand for? 

{% hint style="success" %}
Secure Shell
{% endhint %}

### How do webservers prove their identity?

{% hint style="success" %}
certificates
{% endhint %}

### What is the main set of standards you need to comply with if you store or process payment card details?

{% hint style="success" %}
PCI-DSS
{% endhint %}

## Crucial Crypto Maths

###  What's 30 % 5?

![](../.gitbook/assets/image%20%28144%29.png)

{% hint style="success" %}
0
{% endhint %}

### What's 25 % 7

![](../.gitbook/assets/image%20%28137%29.png)

{% hint style="success" %}
4
{% endhint %}

### What's 118613842 % 9091

![](../.gitbook/assets/image%20%28163%29.png)

{% hint style="success" %}
3565
{% endhint %}

## Types of Encryption

The two main categories of Encryption are symmetric and asymmetric.

**Symmetric encryption** uses the same key to encrypt and decrypt the data. Examples of Symmetric encryption are DES \(Broken\) and AES. These algorithms tend to be faster than asymmetric cryptography, and use smaller keys \(128 or 256 bit keys are common for AES, DES keys are 56 bits long\).

**Asymmetric encryption** uses a pair of keys, one to encrypt and the other in the pair to decrypt. Examples are RSA and Elliptic Curve Cryptography. Normally these keys are referred to as a public key and a private key. Data encrypted with the private key can be decrypted with the public key, and vice versa. Your private key needs to be kept private, hence the name. Asymmetric encryption tends to be slower and uses larger keys, for example RSA typically uses 2048 to 4096 bit keys.

RSA and Elliptic Curve cryptography are based around different mathematically difficult \(intractable\) problems, which give them their strength. More about RSA later.

###  Should you trust DES? Yea/Nay

{% hint style="success" %}
Nay
{% endhint %}

### What was the result of the attempt to make DES more secure so that it could be used for longer?

{% hint style="success" %}
Triple DES
{% endhint %}

### Is it ok to share your public key? Yea/Nay

{% hint style="success" %}
Yea
{% endhint %}

## RSA - Rivest Shamir Adleman

## Establishing Keys Using Asymmetric Cryptography

## Digital signatures and Certificates

## SSH Authentication

## Explaining Diffie Hellman Key Exchange

## PGP, GPG and AES

## The Future - Quantum Computers and Encryption

