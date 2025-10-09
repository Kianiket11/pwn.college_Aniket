# Finding commands


## My solve
**Flag:** ``


```
hacker@path~finding-commands:~$ which win
/challenge/paths/4429/win
hacker@path~finding-commands:~$ cat /challenge/paths/4429/win
#!/bin/bash

/bin/fold -s <<< "Search for the flag in the same directory in which I am located!"
hacker@path~finding-commands:~$ cd /challenge/paths/4429
hacker@path~finding-commands:/challenge/paths/4429$ ls
flag  win
hacker@path~finding-commands:/challenge/paths/4429$ cat flag
pwn.college{Y-OI4LzpltUDiTqUThAD6XkZUxk.01NzEzNxwiM1kjNzEzW}
```

## What I learned


## References 
None.
