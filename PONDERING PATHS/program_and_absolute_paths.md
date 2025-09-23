# Program and Absolute path
The challenge askes us to invoke the absolute path of the run directory where the flag is located, which is under the challenge directory.


## My Solve
**Flag:** `pwn.college{sbckRxXhBIKgx_FIP8GeStpkquC.QX1QTN0wiM1kjNzEzW}`
The challenge suggests that instead of running the brelative path or depending on the shell PATH, the challenge prompt highlights 
that you must use its absolute path (`/challenge/run`) to invoke it.

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{sbckRxXhBIKgx_FIP8GeStpkquC.QX1QTN0wiM1kjNzEzW}
hacker@paths~program-and-absolute-paths:~$ 

```

## What I Learned
I learnt that there are two types of paths present in linux which are absolute path and relative path. 
## References
None.
