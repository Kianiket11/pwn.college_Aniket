# Making Directories

In this challenge we have to make a directory and then a file name college in it to obtain the flag.

## My solve
**Flag:** `pwn.college{onZ3NYm6W3FS76TgQ-ntqwOrpPc.QXxMDO0wiM1kjNzEzW}`

Now as the challenge suggest we first make a directory /tmp/pwn using the mkdir commnand, then we enter the directory using cd 
then we create the college file using the touch command to obtain the flag.

```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{onZ3NYm6W3FS76TgQ-ntqwOrpPc.QXxMDO0wiM1kjNzEzW}
```

## What I learned
I learnt about the mkdir command which is used to create directories and is the short form for make directory.
## References 
None.

