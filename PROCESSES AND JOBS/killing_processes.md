# Killing processes

In this challenge /challenge/run will refuse to run while /challenge/dont_run is running. We have to 
find the dont_run process and kill it.

## My solve
**Flag:** `pwn.college{UlSl0JJXuUGjQpjGCf5V1ksf3F_.QXyQDO0wiM1kjNzEzW}`

As given in the challenge /challenge/dont_run is running and we need to find dont_run process and kill it. Therefore, we 
can just use ps -e | grep /challenge/dont_run to search for the procees and as we can see that the PID of the processes is
136. Now, we can just use the kill command to kill the process.

```
hacker@processes~killing-processes:~$ ps -e | grep /challenge/dont_run
hacker@processes~killing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.1  0.0   1056   640 ?        Ss   17:50   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7  0.0  0.0 231708  2560 ?        S    17:50   0:00 /run/dojo/bin/sleep 6h
root         135  0.0  0.0   5204  3520 ?        S    17:50   0:00 su -c /challenge/.launcher hacker
hacker       136  0.0  0.0 231576  3520 ?        Ss   17:50   0:00 /challenge/dont_run
hacker       137  0.0  0.0 231708  2560 ?        S    17:50   0:00 sleep 6h
hacker       139  0.0  0.0 231576  3520 pts/0    Ss   17:50   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-
hacker       145  0.0  0.0 231940  4160 pts/0    S    17:50   0:00 /run/dojo/bin/bash --login
hacker       156  0.0  0.0 233600  3840 pts/0    R+   17:51   0:00 ps aux
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{UlSl0JJXuUGjQpjGCf5V1ksf3F_.QXyQDO0wiM1kjNzEzW}
```

## What I learned

I learnt about the kill command which as the names suggests is used to kill any process that is running in the background. 
But we need the PID of the process to kill it.

## References 
None.
