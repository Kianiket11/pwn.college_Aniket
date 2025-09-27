# Learing complex usage
In this challenge we need to use the --printfile argument correctly in order to get the flag.

## My solve

Now as the challenge suggests we need to use the --printfile argument correctly to obtain the flag, now what i did was firstly check how 
--printfile works by using --printfile /challenge/DESCRIPTION.md which was given in the challenge, now after this i tried running--printfile /challenge/flag
but there no such file or directory. At last i used the command --printfile /flag which gave me the flag.

**Flag:** `pwn.college{8rCWDT6Uwaz3NYo03eXX0goiQpP.QX1ITO0wiM1kjNzEzW}`

```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/DESCRIPTION.md
Correct argument! Here is the /challenge/DESCRIPTION.md file:
While using most commands is straightforward, the usage of some commands can get quite complex.
For example, the arguments to commands like `sed` and `awk`, which we're definitely not getting into right now, are entire programs in an esoteric programming language!
Somewhere on the spectrum between `cd` and `awk` are commands that take arguments to their arguments...

This sounds crazy, but you've already encountered this with the `find` level in [Basic Commands](/linux-luminarium/commands).
`find` has a `-name` argument, and the `-name` argument itself takes an argument specifying the name to search for.
Many other commands are analogous.

Here is this level's documentation for `/challenge/challenge`:

> Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The argument to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the description of the level!
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/flag
Correct argument! Here is the /challenge/flag file:
cat: /challenge/flag: No such file or directory
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{8rCWDT6Uwaz3NYo03eXX0goiQpP.QX1ITO0wiM1kjNzEzW}

```

## What I learned

I learnt the complex usage of commands and how different arguments work.

## References 
None.
