# Switching windows(tmux)


## My solve
**Flag:** `pwn.college{coWnowCCVEavXNOnIjqn-jlVU-X.0FM5IDOxwiM1kjNzEzW}`


```
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux
hacker@terminal-multiplexing~switching-windows-tmux:~$ ctrl + b d
[detached (from session 1)]
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux attach -t challenge_session
[detached (from session challenge_session)]
ctrl + b + 0
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{coWnowCCVEavXNOnIjqn-jlVU-X.0FM5IDOxwiM1kjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{coWnowCCVEavXNOnIjqn-jlVU-X.0FM5IDOxwiM1kjNzEzW}
```

## What I learned


## References 
None.
