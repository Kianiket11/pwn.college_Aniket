# Switching windows

In this challenge, two screen sessions with two windows have been set up. We need to attach to the session then use one 
of the key combinations to switch to Window 1.

## My solve
**Flag:** `pwn.college{87v4B3Vqf8bTvbU7jOBFNciUlA_.0FO4IDOxwiM1kjNzEzW}`

As the challenge suggests that there have been seesions setup. So i first attached to challenge_session and the used ctrl+ A and 
0, to swith to window 0 and finally got the flag.

```
hacker@terminal-multiplexing~switching-windows:~$ screen -ls
There are screens on:
	150.pts-0.terminal-multiplexing~launching-screen	(Remote or dead)
	176.pts-2.terminal-multiplexing~launching-screen	(Remote or dead)
	139.pts-0.terminal-multiplexing~detaching-and-attaching	(Remote or dead)
	144.session_26ffb5d07bba4904	(Remote or dead)
	147.session_1e8f26f59367c28e	(Remote or dead)
	150.session_cf8915a694c6cd47	(Remote or dead)
	135.challenge_session	(Detached)
7 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~switching-windows:~$ scree -r challenge_session
Welcome to the window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-A 0 to switch to window 0!
MSG
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Welcome to the window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-A 0 to switch to window 0!
> MSG
Welcome to the window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-A 0 to switch to window 0!
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{87v4B3Vqf8bTvbU7jOBFNciUlA_.0FO4IDOxwiM1kjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{87v4B3Vqf8bTvbU7jOBFNciUlA_.0FO4IDOxwiM1kjNzEzW}
```

## What I learned

I learnt about the different keyboard shortcuts that can be used in screen session.

## References 
None.
