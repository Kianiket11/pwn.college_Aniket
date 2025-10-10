# Exexutable shell script

In this challenge we need to make a shellscript that will invoke /challenge/solve, make it executable, and run it 
without explicitly invoking bash.

## My solve
**Flag:** `pwn.college{ILYe4ybLJWTWqrOrfGhJAGMhFUR.QX0cjM1wiM1kjNzEzW}`

As given in the challenge i first made a shellscript using nano and then typed /challenge/solve in to the file. later when
i used ls -l script.sh to view the permissions there was exexute and write permissions were missing. Therefore, I used 
chmod to change the permission and used 777 which gave the required permissions. Finally ran ./script.sh and got the flag.

```
hacker@chaining~executable-shell-scripts:~$ nano script.sh
/challenge/solve
hacker@chaining~executable-shell-scripts:~$ ls -l script.sh
-rw-r--r-- 1 hacker hacker 18 Oct  9 19:09 script.sh
hacker@chaining~executable-shell-scripts:~$ chmod 777 script.sh
hacker@chaining~executable-shell-scripts:~$ ./script.sh
Congratulations on your shell script execution! Your flag:
pwn.college{ILYe4ybLJWTWqrOrfGhJAGMhFUR.QX0cjM1wiM1kjNzEzW}
```

## What I learned

Learnt nothing new but this challenge helped me revise previous the previous modules.

## References 
None.
