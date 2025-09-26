# Linking Files
In this challenge the flag in /flag, but /challenge/catflag will instead read out /home/hacker/not-the-flag. we have to use
symlink and fool it into giving you the flag.

## My solve
**Flag:** `pwn.college{ACRrCJcshS_qXusJk65zADHxKWk.QX5ETN1wiM1kjNzEzW}`

As given in the challenge /challenge/catflag will read out /home/hacker/not-the-flag. therefore we can just swapp the symlink 
to point it towards the /flag, and get the flag.

```
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{ACRrCJcshS_qXusJk65zADHxKWk.QX5ETN1wiM1kjNzEzW}
```

## What I learned
I learnt about the types of links mainly hard and soft. Then i learnt about sybolic links (symlinks) and how symlinks work.
we create a symlink using ln -s command.

## References 
None.

