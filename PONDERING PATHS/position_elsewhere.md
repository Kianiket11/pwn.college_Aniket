# Position Elsewhere 
This challenge asks us to execute the /challenge/run program from a specific path(which a certain directory which it will tell us.
And we'll have to cd the directory to find the path.

## My solve
**Flag:** `pwn.college{gfsroW5t7SOLy0l15EMpYQ2zWOX.QX3QTN0wiM1kjNzEzW}`

This challenge is the same as the previous one. So i basically just did the same thing again, which is i ran cd /home in order 
to find the path in which the flag was hidden.

```
hacker@paths~position-elsewhere:~$ cd /home
hacker@paths~position-elsewhere:/home$ /challenge/run
Incorrect...
You are not currently in the /usr/share/build-essential directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:/home$ cd /usr/share/build-essential
hacker@paths~position-elsewhere:/usr/share/build-essential$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{gfsroW5t7SOLy0l15EMpYQ2zWOX.QX3QTN0wiM1kjNzEzW}
hacker@paths~position-elsewhere:/usr/share/build-essential$ 

```

## What I learned
Didn't learn anything new from this challenge as this is just the practice problem cause we had to use what we learnt from the 
previous problem.

## References 
Add any references or videos u used while solving the challenge.
