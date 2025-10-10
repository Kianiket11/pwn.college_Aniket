# Detaching and attaching(tmux)

In this challenge we need to :

Launch tmux
Detach from it.
Run /challenge/run (this will send the flag to your detached session!)
Reattach to see your prize

## My solve
**Flag:** `pwn.college{wgryCP6i8netxj3uPlANJEMWkq8.0VO4IDOxwiM1kjNzEzW}`

As given in the challenge I first launched tmux and then used ctrl + B then d to detach from it and finally used tmux a 
to reattach and go the flag.

```
hacker@terminal-multiplexing~detaching-and-attaching-tmux: tmux
hacker@terminal-multiplexing~detaching-and-attaching-tmux: ctrl + B then d
hacker@terminal-multiplexing~detaching-and-attaching-tmux: /challenge/run
hacker@terminal-multiplexing~detaching-and-attaching-tmux: tmux a
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ Congratulations, here is your flag: pwn.college{wgryCP6i8netxj3uPlANJEMWkq8.0VO4IDOxwiM1kjNzEzW
```

## What I learned

I learnt about tmux which is the short form for terminal multiplexer.It is called screen's younger, more modern cousin.

## References 
None.
