# Backgrounding processes

In this challenge run wants to see another copy of itself running in the background

## My solve
**Flag:** `pwn.college{gq1Ux98wnLCjTJySCB_dDeYKJYw.QX3QDO0wiM1kjNzEzW}`

As the challenge suggests run wants another copy of itself running in the background, we can do this by first running /challenge/run
then using  ctrl + z to suspend the process and then using bg /challenge/run to run the process in the background. Again, running
/challenge/run to get the flag.

```
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         138 S+   bash /challenge/run
root         140 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         138 S    bash /challenge/run
root         148 S    sleep 6h
root         149 S+   bash /challenge/run
root         151 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{gq1Ux98wnLCjTJySCB_dDeYKJYw.QX3QDO0wiM1kjNzEzW}
```

## What I learned

I learnt about the bg command which can a run a process in the background.

## References 
None.
