# ReverseELFneering

## Video

{% embed url="https://www.youtube.com/watch?v=5X5SHprLHts" %}

## Resources

Start radare2: `r2 -d ./file1`

Analyze the program: `aa`  It analyses all symbols and entry points in the executable

For general help, we can run: `?` or if we wish to understand more about a specific feature, we could provide `a?`

To find a list of the functions run: `afl`

Let’s examine the assembly code at main by running the command `pdf @main` Where `pdf` means print disassembly function.

[Radare2 Cheatsheet](https://scoding.de/uploads/r2_cs.pdf)

## Challenge

**IP Address:** 10.10.83.56

**Username:** elfmceager

**Password:** adventofcyber

```text
ssh elfmceager@10.10.83.56
```

![](../.gitbook/assets/image%20%28114%29.png)

What is the value of **local\_ch** when its corresponding movl instruction is called \(first if multiple\)?

{% hint style="success" %}

{% endhint %}

What is the value of **eax** when the imull instruction is called?

{% hint style="success" %}

{% endhint %}

What is the value of **local\_4h** before **eax** is set to 0?

{% hint style="success" %}

{% endhint %}

