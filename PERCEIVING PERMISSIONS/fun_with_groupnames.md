# Fun with groupnames

In this challenge the name of the group in which the user is present is randomized. We need to find the group name and then
change the group ownership inorder to get the flag.

## My solve
**Flag:** `pwn.college{8XiKD4C7Ae34vTptXNtaONISBGS.QXycjM1wiM1kjNzEzW}`


```
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp24701) groups=1000(grp24701)
hacker@permissions~fun-with-groups-names:~$ chgrp grp24701 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{8XiKD4C7Ae34vTptXNtaONISBGS.QXycjM1wiM1kjNzEzW}
```

## What I learned


## References 
None.
