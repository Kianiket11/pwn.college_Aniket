# Finding commands

In this challenge a win command somewhere added in our $PATH, but it won't give us the flag. Instead, it's in the 
same directory as a flag file that we made readable by you! We must find win, and cat the flag out of that directory.

## My solve
**Flag:** `pwn.college{Y-OI4LzpltUDiTqUThAD6XkZUxk.01NzEzNxwiM1kjNzEzW}`

As the challenge suggested I first used which win to find the exact file location and then i ran cat /challenge/paths/4429/win
but couldn't find the flag so I cd to /challenge/paths/4429 and there I found the flag.

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
