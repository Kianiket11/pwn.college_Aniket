# Redirecting script ouput

In this challenge we need to create a script that calls the /challenge/pwn command followed by the /challenge/college command, 
and pipe the output of the script into a single invocation of the /challenge/solve command

## My solve
**Flag:** `pwn.college{AI7DiEvB2aSeZ3c8pH2sNeMLX9c.QX4ETO0wiM1kjNzEzW}`

As the challenge suggests that first we need to create a script and then call the commands like we did in the previous challenge.
Therefore, we can do this by first using nano and creating a script called flag.sh and later using pipe to pipe the output which is
the flag.

```
hacker@chaining~your-first-shell-script:~$ nano flag.sh
hacker@chaining~your-first-shell-script:~$ ls -l flag.sh
-rw-r--r-- 1 hacker hacker 37 Oct  9 18:53 flag.sh
hacker@chaining~your-first-shell-script:~$ bash flag.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{AI7DiEvB2aSeZ3c8pH2sNeMLX9c.QX4ETO0wiM1kjNzEzW}

```

## What I learned

Learnt nothing new as the challenge was similar to what we did in the earlier challenge.

## References 
None.
