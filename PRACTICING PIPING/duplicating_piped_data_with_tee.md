# Duplicating piped data with tee

In this challenge /challenge/pwn must be piped into /challenge/college, but we need to intercept the data to see what pwn.

## My solve
**Flag:** `pwn.college{4hITxNwn3eNNZBxLHok28544ASS.QXxITO0wiM1kjNzEzW}`

As the challenge suggests first we nedd to intercept pwn. therefore, i used cat. and then i used /challenge/pwn --secret 4hITxNwn,
but here i forgot to pipe /challenge/pwn to /challenge/college and got an error. Finalle, used 
/challenge/pwn --secret 4hITxNwn | /challenge/college in order to get the flag.
```
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "4hITxNwn"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/run --secret 4hITxNwn 
bash: /challenge/run: No such file or directory
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret 4hITxNwn 
Processing...
You must pipe the output of /challenge/pwn into /challenge/college (or 'tee' 
for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret 4hITxNwn | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{4hITxNwn3eNNZBxLHok28544ASS.QXxITO0wiM1kjNzEzW}
```

## What I learned

I learnt about the tee command which is named after a "T-splitter" from plumbing pipes. I learnt that this command duplicates the data 
flowing through the pipes to any number of files that are provided in the command line.

## References 
None.
