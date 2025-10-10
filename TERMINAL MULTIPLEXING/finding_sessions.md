# Finding sessions

In this challenge thre are three screen sessions for us. One of them contains the flag. The other two are decoys. We have to attach
to the correct screen in order to get the flag.

## My solve
**Flag:** ``

As given in the challenge that there are three screen sessions, which we can see by running screen -ls. Now as one of them
was the correct one so I attached the second screen session and it was the correct one and i got the flag.

```
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        150.pts-0.terminal-multiplexing~launching-screen        (Remote or dead)
        176.pts-2.terminal-multiplexing~launching-screen        (Remote or dead)
        139.pts-0.terminal-multiplexing~detaching-and-attaching (Remote or dead)
        144.session_26ffb5d07bba4904    (Detached)
        147.session_1e8f26f59367c28e    (Detached)
        150.session_cf8915a694c6cd47    (Detached)
6 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_1e8f26f59367c28e 
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{ojq0uNsPMUw5fmD5pjTXBBDQHSv.01N4IDOxwiM1kjNzEzW}
pwn.college{ojq0uNsPMUw5fmD5pjTXBBDQHSv.01N4IDOxwiM1kjNzEzW}
```

## What I learned

I learnt how we can list screen sessions that are currently preesent in our terminal.

## References 
None.
