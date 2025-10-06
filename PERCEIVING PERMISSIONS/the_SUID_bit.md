# The SUID bit

In this challenge we need to add the SUID bit to the /challenge/getroot program in order to spawn a root shell and cat the flag.

## My solve
**Flag:** `pwn.college{gwPcxJU90sQKQ0uUpg5UoPnVkUZ.QXzEjN0wiM1kjNzEzW}`

As given in the challenge we need to add the SUID bit to /challenge/getroot. We can do this by using chmod u+s command.

```
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{gwPcxJU90sQKQ0uUpg5UoPnVkUZ.QXzEjN0wiM1kjNzEzW}
```

## What I learned

I learnt about the SUID bit which stands for "Set User ID". What SUID does is it allows the user to run a program as 
the owner of that program's file.

## References 
None.
