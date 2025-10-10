# Switching windows(tmux)

In this challenge, Atmux sessions with two windows have been set up. We need to first detacha then reattach to the session 
then use one of the key combinations to switch to Window 0.

## My solve
**Flag:** `pwn.college{coWnowCCVEavXNOnIjqn-jlVU-X.0FM5IDOxwiM1kjNzEzW}`

As given in the challenge first i ran tmux and then used ctrl + b d to detach and then tmux attach -t to reattach to the session
and then used ctrl + b + 0 to switch to window 0 and finally got the flag.

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

I learnt about the different key combinations used in tmux.

## References 
None.
