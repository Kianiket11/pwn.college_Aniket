# Your first shell script

In this challenge we need to run /challenge/pwn and then /challenge/college, but this time in a shell script 
called x.sh, then run it with bash

## My solve
**Flag:** `pwn.college{UiOOWAn2gsZy0PS-ALD6dKH_IyA.QXxcDO0wiM1kjNzEzW}`

As the challenge suggests that we need to run /challenge/pwn and /challenge/college but in a shell script called x.sh. 
What i did is, I used the GNU nano text editor and there i wrote /challenge/pwn ; /challenge/college and later ran bash
x.sh in order to get the flag.

```
hacker@chaining~your-first-shell-script:~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{UiOOWAn2gsZy0PS-ALD6dKH_IyA.QXxcDO0wiM1kjNzEzW}
```

## What I learned

I learnt about shell scripts and how we can put commands into a file. I also learnt about nano which is a 
pretty common text editor used in linux. 

## References 
https://www.youtube.com/watch?v=DLeATFgGM-A
