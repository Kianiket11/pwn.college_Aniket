# Suspending processes

In this challenge run wants to see another copy of itself running and using the same terminal. 


## My solve
**Flag:** `pwn.college{IO00CGK_euZ1iMigvCzYVfhld2e.QX1QDO0wiM1kjNzEzW}`

As the challenge suggests that run wants to see another copy of itself running we can do this by first suspending the 
current run using ctrl + z and then running run again so that there is another copy of itself in the same terminal.

```
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         141     129  0 18:10 pts/0    00:00:00 bash /challenge/run
root         143     141  0 18:10 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         141     129  0 18:10 pts/0    00:00:00 bash /challenge/run
root         148     129  0 18:10 pts/0    00:00:00 bash /challenge/run
root         150     148  0 18:10 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{IO00CGK_euZ1iMigvCzYVfhld2e.QX1QDO0wiM1kjNzEzW}
```

## What I learned

I learnt that we can suspend processes to the background with Ctrl-Z.

## References 
None.
