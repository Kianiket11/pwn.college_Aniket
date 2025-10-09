# Scripting with default cases 


## My solve
**Flag:** `pwn.college{IxLXBEaoA3jcXFaXIz3Jy10VgGa.01NzMDOxwiM1kjNzEzW}`


```
hacker@chaining~scripting-with-default-cases:~$ nano /home/hacker/solve.sh
#!/bin/bash
if [ "$1" == "pwn" ]
then
    echo "college"
else
    echo "nope"
fi

hacker@chaining~scripting-with-default-cases:~$ ./solve.sh pwn
college
hacker@chaining~scripting-with-default-cases:~$ ./solve.sh hack
nope
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{IxLXBEaoA3jcXFaXIz3Jy10VgGa.01NzMDOxwiM1kjNzEzW}
```

## What I learned


## References 
None.
