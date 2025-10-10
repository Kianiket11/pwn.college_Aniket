# Detaching and attaching 

In this challenge we need to:

Launch screen
Detach from it.
Run /challenge/run (this will secretly send the flag to your detached session!)
Reattach to see your prize

## My solve
**Flag:** ``

As the challenge suggest first I launched screen using the screen command and then I pressd ctrl + A then d to detach from it and
lastly ran screen -r to reattach and got the flag.

```
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen
hacker@terminal-multiplexing~detaching-and-attaching:~$ ctrl + A then d
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{o-Mtven3PpvHk921Ax5lt4nBztX.0lN4IDOxwiM1kjNzEzW}
Yes! Flag is: pwn.college{o-Mtven3PpvHk921Ax5lt4nBztX.0lN4IDOxwiM1kjNzEzW}
```

## What I learned

I learnt how to detach and reattach a scrren.

## References 
None.
