---
description: 'https://tryhackme.com/room/agentsudoctf'
---

# Agent Sudo

## INIT

```text
export agentsudo=10.10.150.200
ping $agentsudo

echo "10.10.150.200 agentsudo.thm" >> /etc/hosts
```



## NMAP

```text
nmap -v -sC -sV -O -T5 -p1-65535 pickle.thm
```

