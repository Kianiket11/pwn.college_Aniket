# Groups and files

In this challenge we need to change the group ownership of the flag file to hacker user and read the flag.

## My solve
**Flag:** `pwn.college{4nV2Rrm3u0TTjn-7yAdO-MtDZRY.QXxcjM1wiM1kjNzEzW}`

As given in the challenge that we need to change the group owner of the /flag file. We can do this by using the 
chgrp hacker /flag command in order to read the flag.

```
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{4nV2Rrm3u0TTjn-7yAdO-MtDZRY.QXxcjM1wiM1kjNzEzW}
```

## What I learned

I learnt about chgrp command which is basically the short form for change group, and as the name suggests this 
command is used to change the ownership of a group. I also learnt about the id command which can be used to check 
what groups you are part of.


## References 
None.
