# Starting backgrounded processes

In this challenge we need launch /challenge/run backgrounded for the flag without suspending the process.

## My solve
**Flag:** `pwn.college{Ep58T1XFbwxLD4emY4L2k65oRVD.QX5QDO0wiM1kjNzEzW}`

As the challenge suggests that we need /challenge/run to be backgrounded without suspending the process, we can do this by using 
& with the /challenge/run. It will start /challenge/run in the background without suspending it.

```
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 138
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{Ep58T1XFbwxLD4emY4L2k65oRVD.QX5QDO0wiM1kjNzEzW}

[1]+  Done                    /challenge/run

```

## What I learned

I learnt about & which when used with a command causes it to start in the background.

## References 
None.
