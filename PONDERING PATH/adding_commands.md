# Adding commands

In this challenge 

## My solve
**Flag:** `pwn.college{8N4R0dTvhYSIsQCfGX1DJrUJUIr.QX2cjM1wiM1kjNzEzW}`


```
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ cat win
!#/bin/bash
read flag < /flag
echo "$flag"

hacker@path~adding-commands:~$ chmod 777 in
chmod: cannot access 'in': No such file or directory
hacker@path~adding-commands:~$ chmos 777 win
bash: chmos: command not found
hacker@path~adding-commands:~$ chmod 777 win
hacker@path~adding-commands:~$  PATH=/home/hacker
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
/home/hacker/win: line 1: !#/bin/bash: No such file or directory
pwn.college{8N4R0dTvhYSIsQCfGX1DJrUJUIr.QX2cjM1wiM1kjNzEzW}
```

## What I learned


## References 
None.
