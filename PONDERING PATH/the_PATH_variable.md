# The PATH variable

In this challenge we need to disrupt the operation of the /challenge/run program. This program will DELETE the flag file 
using the rm command. However, if it can't find the rm command, the flag will not be deleted, and the challenge will give it to us.

## My solve
**Flag:** `pwn.college{EDWBORz7_HTFF1y7_n6imuEdxKs.QX2cDM1wiM1kjNzEzW}`

As given in the challenge that we need to disrupt the operation of the /challenge/run program. Therefore, I just set 
the PATH = "challenge/run". Then i ran /challenge/run and it cannot find the rm command so we got the flag.

```
hacker@path~the-path-variable:~$ PATH="/challenge/run"
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: command not found
The flag is still there! I might as well give it to you!
pwn.college{EDWBORz7_HTFF1y7_n6imuEdxKs.QX2cDM1wiM1kjNzEzW}
```

## What I learned

I learnt about PATH which is a special shell variable that stores a bunch of directory paths in which the 
shell will search for programs corresponding to commands. 

## References 
None.
