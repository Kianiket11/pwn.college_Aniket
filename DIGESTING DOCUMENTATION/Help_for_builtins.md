# Help for builtins
In this challenge the challenge command is a shell builtin, rather than a program and like before we need to lookup its help to figure out the 
secret value to get the flag

## My solve
**Flag:** `pwn.college{cJKNDvFEZ58xLunN5M7qhg0p1Ex.QX0ETO0wiM1kjNzEzW}`

As the challenge suggests, we have to use the builtin help as the challenge command is also a shell buitin.Therefore, we get the secret value.
Finally, we just have to use the --secret cJKNDvFE to get the flag.

```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "cJKNDvFE".
hacker@man~help-for-builtins:~$ challenge --secret cJKNDvFE
Correct! Here is your flag!
pwn.college{cJKNDvFEZ58xLunN5M7qhg0p1Ex.QX0ETO0wiM1kjNzEzW}
```

## What I learned

I learnt that some commands,rather than being programs with man pages and help options, are built into the shell itself. These are called builtins. 
Builtins are invoked just like commands, but the shell handles them internally instead of launching other programs. we can get a list of shell builtins 
by running the builtin help.

## References 
None.
