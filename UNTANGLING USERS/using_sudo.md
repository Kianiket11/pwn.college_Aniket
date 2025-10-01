# Using sudo


## My solve
**Flag:** `pwn.college{c8yAbeJ15o0Fg5oe4D9uVFFproo.QX4UDN1wiM1kjNzEzW}`


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


## References 
None.
