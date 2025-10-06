# Changing file ownership

In this challenge we need to change the owner of the /flag file to the hacker user, and then read the flag.

## My solve
**Flag:** `pwn.college{8tMIUGcvUbSqmWcS23gdVo-3X_Y.QXxEjN0wiM1kjNzEzW}`

As given in the challenge that we need to change the owner of the /flag file in order to get the flag. We can do this
by using the chown hacker /flag command. 

```
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{8tMIUGcvUbSqmWcS23gdVo-3X_Y.QXxEjN0wiM1kjNzEzW}
```

## What I learned

I learnt about the chown command, which is the short form of change owner and as the name suggests it is used to change
the owner of a given file 

## References 
None.
