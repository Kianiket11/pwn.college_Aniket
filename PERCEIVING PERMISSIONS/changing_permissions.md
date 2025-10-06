# Changing permissions

In this challenge we need to change the permissions of the /flag file to read it.

## My solve
**Flag:** `pwn.college{sds_nZy0tC8UWF9y4LYKW5yiW3a.QXzcjM1wiM1kjNzEzW}`

As given in the challenge that we need to change the permissions of the /flag in order to read it. Therefore, I used chmod command with u+r 
which gives read access to the user's permissions. Now, as we have the read access, we can now read the flag.

```
hacker@permissions~changing-permissions:~$ chmod go-u+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{sds_nZy0tC8UWF9y4LYKW5yiW3a.QXzcjM1wiM1kjNzEzW}
```

## What I learned

I learnt about the the chmod command which is the short form for change mode and as the name suggest this command allows us to tweak permissions with the mode format
of WHO+/-WHAT, where WHO is user/group/other and WHAT is read/write/execute. 

## References 
None.
