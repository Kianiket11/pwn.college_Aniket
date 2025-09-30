# Process exit code 


## My solve
**Flag:** `pwn.college{0DS9FqTzA4W1wzwlzvRUz1WFSJt.QX5YDO1wiM1kjNzEzW}`


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


## References 
None.
