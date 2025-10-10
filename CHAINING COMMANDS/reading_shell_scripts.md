# Reading shell scripts

In this challenge /challenge/run is a shell script that requires us to put in a secret password, but that password 
is hardcoded into the script iself! We need to read the script (using, say, cat), figure out the password, and get the flag!

## My solve
**Flag:** `pwn.college{Q16vPQPgW1WYmXpiQok9Cx8B1Lr.0lMwgDOxwiM1kjNzEzW}`

As given in the challenge used cat to read /challenge/run there I found that 
if[ "$GUESS" == "hack the PLANET"
then
	echo "CORRECT! Your flag:"
from here i got that the password is hack the planet and then I typed the password in order to get the flag.

```
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
	echo "CORRECT! Your flag:"
	cat /flag
else
	echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{Q16vPQPgW1WYmXpiQok9Cx8B1Lr.0lMwgDOxwiM1kjNzEzW}
```

## What I learned

I learnt how to read shell scripts.

## References 
None.
