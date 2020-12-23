---
description: Forensics
---

# The Grinch strikes again!

## Video

{% embed url="https://www.youtube.com/watch?v=rY1qsQIOl8I" %}

## Resources

The Volume Shadow Copy Service \(VSS\) coordinates the actions that are required to create a consistent shadow copy \(also known as a snapshot or a point-in-time copy\) of the data that is to be backed up.

The command to interact with VSS is `vssadmin`. Running the command alone will display brief information on how to run the utility with additional commands. Two commands of particular interest are `List Volumes` and `List Shadows`.

## Challenge

Decrypt the fake 'bitcoin address' within the ransom note. What is the plain text value?

{% hint style="success" %}

{% endhint %}

At times ransomware changes the file extensions of the encrypted files. What is the file extension for each of the encrypted files?

{% hint style="success" %}

{% endhint %}

What is the name of the suspicious scheduled task?

{% hint style="success" %}

{% endhint %}

Inspect the properties of the scheduled task. What is the location of the executable that is run at login?

{% hint style="success" %}

{% endhint %}

There is another scheduled task that is related to VSS. What is the ShadowCopyVolume ID?

{% hint style="success" %}

{% endhint %}

Assign the hidden partition a letter. What is the name of the hidden folder?

{% hint style="success" %}

{% endhint %}

Right-click and inspect the properties for the hidden folder. Use the 'Previous Versions' tab to restore the encrypted file that is within this hidden folder to the previous version. What is the password within the file?

{% hint style="success" %}

{% endhint %}

