# Helpful programs
In this challenge we have to practice reading a program's documentation with --help. 

## My solve
**Flag:** `pwn.college{UixeU25dLYUdIR9UHFfcwobkZr6.QX3IDO0wiM1kjNzEzW}`

In this we just have to use the -h/--help argument to find the flag. so we jus the follow the same steps as previous as after using -h we 
get -p which prints the value that will cause the -g option to give us the flag.Finally, we use -g with the value that we got with - p in order 
to get the flag.

```
hacker@man~helpful-programs:~$ /challenge/challenge -h
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 259
hacker@man~helpful-programs:~$ /challenge/challenge -g 259
Correct usage! Your flag: pwn.college{UixeU25dLYUdIR9UHFfcwobkZr6.QX3IDO0wiM1kjNzEzW}
```

## What I learned
I learnt that Some programs don't have a man page, but might tell you how to run them if invoked with a special argument. 
Usually, this argument is --help, but it can often be -h also.

## References 
None.
