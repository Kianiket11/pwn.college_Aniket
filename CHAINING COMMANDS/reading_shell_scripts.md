# Reading shell scripts


## My solve
**Flag:** `pwn.college{Q16vPQPgW1WYmXpiQok9Cx8B1Lr.0lMwgDOxwiM1kjNzEzW}`


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


## References 
None.
