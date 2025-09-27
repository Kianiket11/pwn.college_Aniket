# Exclusionary globbing 

In this challenge we have to go forth to /challenge/files and then run /challenge/run with all files that don't start with p, w, or n.

## My solve
**Flag:** `pwn.college{ooPaAqjGgaaBZF-eAH935arNvMi.QX2IDO0wiM1kjNzEzW}`

As 

```
hacker@globbing~exclusionary-globbing:/challenge$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ echo look [!pwn]*
look amazing beautiful challenging delightful educational fantastic great happy incredible jovial kind laughing magical optimistic queenly radiant splendid thrilling uplifting victorious xenial youthful zesty
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{ooPaAqjGgaaBZF-eAH935arNvMi.QX2IDO0wiM1kjNzEzW}
```

## What I learned


## References 
None.
