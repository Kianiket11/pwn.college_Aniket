# Intro To The Root
This challenge is the basic introduction to how we can access files in linux. Here root is the top most directory of the entire filesystem,
And all the other files branch out from here. In this challenge we just had to inko pwn in '/'.

## My Solve
**Flag:**  `pwn.college{Acq5RwY-rMm6MkzHezmlm1Rovuj.QX4cTO0wiM1kjNzEzW}`

We just had to execute /pwn as it was given that the flag in the pwn directory which is in the root (/) directory.
```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{Acq5RwY-rMm6MkzHezmlm1Rovuj.QX4cTO0wiM1kjNzEzW}
hacker@paths~the-root:~$ 


```

## What I Learned
I learnt that how the filesystems work in linux and  the difference between files and directories. I also learnt what a root directory is and 
how we can access different files and directories from the terminal.

## References
None.
