# Setting PATH

In this challenge /challenge/run will run the win command via its bare name, but this command exists in the 
/challenge/more_commands/ directory, which is not initially in the PATH. The win command is the only thing that 
/challenge/run needs, so we can just overwrite PATH with that one directory. 

## My solve
**Flag:** `pwn.college{ov5WzvgMiM_iKEJqKV4oDY4guJA.QX1cjM1wiM1kjNzEzW}`

As given in the challenge i just set the PATH to /challenge/more_commands/ directory, which is not initially in the PATH. Then i 
ran /challenge/run and finally got the flag.

```                                                                      
hacker@path~setting-path:~$ PATH=/challenge/more_commands/ 
hacker@path~setting-path:~$ win
It looks like 'win' was improperly launched. Don't launch it directly; it MUST 
be launched by /challenge/run!
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{ov5WzvgMiM_iKEJqKV4oDY4guJA.QX1cjM1wiM1kjNzEzW}
```

## What I learned

I learnt more about how does PATH works.

## References 
None.
