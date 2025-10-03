# Using sudo

In this challenge we'll be given sudo access and you we have to  use it to read the flag.

## My solve
**Flag:** `pwn.college{c8yAbeJ15o0Fg5oe4D9uVFFproo.QX4UDN1wiM1kjNzEzW}`

As given in the we need to find the flag using sudo. Now, what i did was i started searching for the flag randomly but  
i wasn't able to find the flag. Then i started my search from root library in order to find the flag. Finally, I was
able to find the flag in the root library.

```
hacker@users~using-sudo:/$ sudo cat /challenge/run
#!/bin/bash
hacker@users~using-sudo:/$ sudo cat/challenge/flag
sudo: cat/challenge/flag: command not found
hacker@users~using-sudo:/$ sudo cat /challenge/flag
cat: /challenge/flag: No such file or directory
hacker@users~using-sudo:~$ cd /
hacker@users~using-sudo:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@users~using-sudo:/$ sudo cat /flag
pwn.college{c8yAbeJ15o0Fg5oe4D9uVFFproo.QX4UDN1wiM1kjNzEzW}
```

## What I learned

I learnt about sudo which meaans "substitute user, do". I learnt that sudo defaults to running a command as root.

## References 
None.
