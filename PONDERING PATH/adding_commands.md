# Adding commands

In this challenge win does not exist. we need to make a shell script called win, and add its location to the PATH, 
and enable /challenge/run to ge the flag.

## My solve
**Flag:** `pwn.college{8N4R0dTvhYSIsQCfGX1DJrUJUIr.QX2cjM1wiM1kjNzEzW}`

As given in the challenge i used nano to create a shell script and added !#/bin/bash read flag < /flag echo "$flag" to it.
then i changed the permissions and lastly set the path to /home/hacker to finally get the flag.

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

Learnt nothing new but this challenge helped me revise and practice what I learned previously.

## References 
None.
