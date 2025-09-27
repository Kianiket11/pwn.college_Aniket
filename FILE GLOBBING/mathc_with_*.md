# Match with *

In this challenge we have to change our directory to /challenge, by using globbing to keep the argument we pass to cd 
to at most four characters.

## My solve

**Flag:** `pwn.college{EroGY7UsUgIQuevNSMN60-7MDZg.QXxIDO0wiM1kjNzEzW}`

As given in the challenge we have to use globing but only upto 4 characters.So, I used cd /ch* to change directories which
changed te directory to challenge and after reaching there i just ran /challenge/run to get the flag.

```
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{EroGY7UsUgIQuevNSMN60-7MDZg.QXxIDO0wiM1kjNzEzW}
```

## What I learned
I learnt about * glob, it works as when it encounters a * character in any argument, the shell will treat it as a "wildcard"
and try to replace that argument with any files that match the pattern.

## References 
None.
