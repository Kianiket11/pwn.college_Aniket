# Switching windows


## My solve
**Flag:** `pwn.college{87v4B3Vqf8bTvbU7jOBFNciUlA_.0FO4IDOxwiM1kjNzEzW}`


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


## References 
None.
