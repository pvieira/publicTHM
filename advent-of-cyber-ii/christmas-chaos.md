---
description: Web Exploitation - Burp Suite
---

# Christmas Chaos

## Web Exploitation

{% embed url="https://www.youtube.com/watch?v=cQq6xPCZFjg&" %}

Deploy your AttackBox

{% hint style="success" %}
No answer needed
{% endhint %}

![](../.gitbook/assets/image%20%2816%29.png)

Use Burp Suite as proxy and intercept the request in Burp Suite.

![](../.gitbook/assets/image%20%2810%29.png)

**`Send to Intruder`** --&gt; **`Positions`**

Select **`Attack Type`** **`Cluster Bomb`**

Use BurpSuite to brute force the login form. Use the following lists for the default credentials: 

| Username | Password |
| :--- | :--- |
| root | root |
| admin | password |
| user | 12345 |

**`Payloads`**

![](../.gitbook/assets/image%20%281%29.png)

![](../.gitbook/assets/image.png)

`Start attack`

![](../.gitbook/assets/image%20%2820%29.png)

Looking at the results, the pair **`admin`** **`12345`** as a different size lenght result.

![](../.gitbook/assets/image%20%2817%29.png)

Use the correct credentials to log in to the Santa Sleigh Tracker app. Don't forget to turn off Foxyproxy once BurpSuite has finished the attack!

![](../.gitbook/assets/image%20%282%29.png)

What is the flag?

{% hint style="success" %}
THM{885ffab980e049847516f9d8fe99ad1a}
{% endhint %}

