# Interrupting processes

In this challenge we need to interrupt /challenge/run as it will refuse to give us the flag until we interrupt it. 

## My solve
**Flag:** `pwn.college{cYy5zOwS2eLg0ufUByb20n45IZo.QXzQDO0wiM1kjNzEzW}`

As given in the challenge we need to interrupt /challenge/run to get the flag we can do this by using ctrl + c. 

```
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{cYy5zOwS2eLg0ufUByb20n45IZo.QXzQDO0wiM1kjNzEzW}
```

## What I learned

I learnt that ctrl + c is used to interrupt/ stop a running process.

## References 
None.
