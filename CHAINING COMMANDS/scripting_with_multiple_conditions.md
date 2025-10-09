# Scripting with multiple conditions


## My solve
**Flag:** `pwn.college{IyuhNOGuqHAyB0XkGWmaZIQCXcw.0FOzMDOxwiM1kjNzEzW}`


```
hacker@chaining~scripting-with-multiple-conditions:~$ nano /home/hacker/solve.sh
#!/bin/bash
if [ "$1" == "hack" ]
then
    echo "the planet"
elif [ "$1" == "pwn" ]
then
    echo "college"
elif [ "$1" == "learn" ]
then
    echo "linux"
else
    echo "unknown"
fi
hacker@chaining~scripting-with-multiple-conditions:~$ ./solve.sh hack
the planet
hacker@chaining~scripting-with-multiple-conditions:~$ ./solve.sh pwn
college
hacker@chaining~scripting-with-multiple-conditions:~$ ./solve.sh learn
linux
hacker@chaining~scripting-with-multiple-conditions:~$ ./solve.sh foo
unknown
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{IyuhNOGuqHAyB0XkGWmaZIQCXcw.0FOzMDOxwiM1kjNzEzW}
```

## What I learned


## References 
None.
