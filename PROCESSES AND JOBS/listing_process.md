# Challenge Name


## My solve
**Flag:** `pwn.college{gkfw--P8K4YGaKJd445n1bAlzZa.QX4MDO0wiM1kjNzEzW}`


```
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 17:46 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 17:46 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 17:46 ?        00:00:00 /challenge/20654-run-21550
root         135     132  0 17:46 ?        00:00:00 sleep 6h
hacker       137       0  0 17:46 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint
hacker       143     137  0 17:46 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       153     143  0 17:47 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   17:46   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7  0.0  0.0 231708  2560 ?        S    17:46   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ?        S    17:46   0:00 /challenge/20654-run-21550
root         135  0.0  0.0   2744  1600 ?        S    17:46   0:00 sleep 6h
hacker       137  0.0  0.0 231576  3520 pts/0    Ss   17:46   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-
hacker       143  0.0  0.0 231940  4160 pts/0    S    17:46   0:00 /run/dojo/bin/bash --login
hacker       154  0.0  0.0 233600  3840 pts/0    R+   17:47   0:00 ps aux
hacker@processes~listing-processes:~$ /challenge/20654-run-21550
Yahaha, you found me! Here is your flag:
pwn.college{gkfw--P8K4YGaKJd445n1bAlzZa.QX4MDO0wiM1kjNzEzW}
Now I will sleep for a while (so that you could find me with 'ps')
```

## What I learned


## References 
None.
