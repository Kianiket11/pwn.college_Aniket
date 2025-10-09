# Scripting with conditionals


## My solve
**Flag:** `pwn.college{Ap63BaoDxIHxWn8-OYmZpl5tdRa.0lNzMDOxwiM1kjNzEzW}`


```
hacker@chaining~scripting-with-conditionals:~$ nano /home/hacker/solve.sh
#!/bin/bash
if [ "$1" == "pwn" ]
then
    echo "college"
fi

hacker@chaining~scripting-with-conditionals:~$ ./solve.sh pwn
college
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{Ap63BaoDxIHxWn8-OYmZpl5tdRa.0lNzMDOxwiM1kjNzEzW}
```

## What I learned


## References 
None.
