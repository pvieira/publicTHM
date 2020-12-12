---
description: Web Exploitation - gobuster ; wfuzz
---

# Santa's watching

## Web Exploitation

{% embed url="https://www.youtube.com/watch?v=7GAFQdYCk5s" %}

`gobuster dir -u` [`http://example.com`](http://example.com) `-w wordlist.txt -x php,txt,html`

`wfuzz -c -z file,/usr/share/wordlists/dirb/big.txt localhost:80/FUZZ/note.txt`

`wfuzz -c -z file,mywordlist.txt -d “username=FUZZ&password=FUZZ” -u http://shibes.thm/login.php`

Deploy your AttackBox 

{% hint style="success" %}
No answer needed
{% endhint %}

Given the URL "[http://shibes.xyz/api.php](http://shibes.xyz/api.php)", what would the entire wfuzz command look like to query the "breed" parameter using the wordlist "big.txt" \(assume that "big.txt" is in your current directory\)

Note: For legal reasons, do not actually run this command as the site in question has not consented to being fuzzed!

{% hint style="success" %}
wfuzz -c -z file,big.txt [http://shibes.xyz/api.php?breed=FUZZ](http://shibes.xyz/api.php?breed=FUZZ)
{% endhint %}

Use GoBuster \(against the target you deployed -- not the shibes.xyz domain\) to find the API directory. What file is there?

{% hint style="success" %}
site-log.php
{% endhint %}

Fuzz the date parameter on the file you found in the API directory. What is the flag displayed in the correct post?

{% hint style="success" %}
THM{D4t3\_AP1}
{% endhint %}

