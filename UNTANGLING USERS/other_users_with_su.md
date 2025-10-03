# Other users with su

In this challenge we need to switch to the zardus user and then run /challenge/run. Password is dont-hack-me. 

## My solve
**Flag:** `pwn.college{kOjXtPFouvfQzqT1baFdyc84XlP.QX2UDN1wiM1kjNzEzW}`

As given in the challenge we need to change the user to zardus we can do this by using su zardus and then using the password
dont-hack-me. Finally running /challenge/run in order to get the flag.

```
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{kOjXtPFouvfQzqT1baFdyc84XlP.QX2UDN1wiM1kjNzEzW}
```

## What I learned

I learnt how we can switch to a particular user using su.

## References 
None.

