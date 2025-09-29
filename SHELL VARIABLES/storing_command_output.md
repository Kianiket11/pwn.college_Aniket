# Storing command output

In this challenge we need to read the output of the /challenge/run command directly into a variable called PWN.

## My solve
**Flag:** `pwn.college{gr0Kh1YwZjQhEoqeIEmcFSyJ6il.QX1cDN1wiM1kjNzEzW}`

As given in the challenge first we need to read the output of /challenge/run to a variable PWN. Which can be done with
PWN=$(/challenge/run).

```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo "$PWN"
pwn.college{gr0Kh1YwZjQhEoqeIEmcFSyJ6il.QX1cDN1wiM1kjNzEzW}
```

## What I learned

I learnt how we can read output to a variable.


## References 
None.
