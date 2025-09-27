# Reading Manuals

In this challenge, The challenge in this level has a secret option that, when you use it, will cause the challenge to print the flag. we have to learn 
this option through the man page for challenge.

## My solve
**Flag:** `pwn.college{snglAtyLWetxJXpDj1HmB6F-qDq.QX0EDO0wiM1kjNzEzW}`

Firstly we had to read the manual of challenge in order to learn the commands that will help us find the flag.So, in the description section we can see that
--snglty NUM is used to print the flag if NUM is 160.Therefore, i used this command and changed NUM to 160 in order to obtain the flag.

```
hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                                                          Challenge Commands                                                         CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --snglty NUM
              print the flag if NUM is 160

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                                                                May 2024                                                              CHALLENGE(1)
 Manual page challenge(1) line 1/31 (END) (press h for help or q to quit)

hacker@man~reading-manuals:~$ /challenge/challenge --snglty NUM
Incorrect usage! Please read the challenge man page!
hacker@man~reading-manuals:~$ /challenge/challenge --snglty 160
Correct usage! Your flag: pwn.college{snglAtyLWetxJXpDj1HmB6F-qDq.QX0EDO0wiM1kjNzEzW}

```

## What I learned
I learnt about the man command which is the shortform of manual and as the name suggests, man command is used to check the manual of a particular command
and then we can read about the command.

## References 
None.
