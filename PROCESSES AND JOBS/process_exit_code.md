# Process exit code 

In this challenge we need to retrieve the exit code returned by /challenge/get-code and then run 
/challenge/submit-code with that error code as an argument. 

## My solve
**Flag:** `pwn.college{0DS9FqTzA4W1wzwlzvRUz1WFSJt.QX5YDO1wiM1kjNzEzW}`

As the challenge suggests first we need to run /challenge/get-code which will cause it to exit with an exit code then
we need to run /challenge/submit-code with the exit code as an argument. Now, what i did was i used echo "$?" which 
printed the exit code but after running echo the exit code changes as echo is a new command which caused the error. 
Finally i ran /challenge/submit-code with "$?" due to which "$?" didn't overwrite the error code and i got the flag.

```
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
53
hacker@processes~process-exit-codes:~$ /challenge/submit-code -53
Incorrect... Make sure to use $? immediately after running /challenge/get-code. 
Your shell will overwrite the $? variable with the exit value of any other 
command you run!
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ /challenge/submit-code $?
CORRECT! Here is your flag:
pwn.college{0DS9FqTzA4W1wzwlzvRUz1WFSJt.QX5YDO1wiM1kjNzEzW}
```

## What I learned

I learnt about exit codes and how we can access these exit codes with $?.

## References 
None.
