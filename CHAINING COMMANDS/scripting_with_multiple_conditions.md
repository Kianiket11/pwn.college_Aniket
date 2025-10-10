# Scripting with multiple conditions

In this challenge we need to write a script at /home/hacker/solve.sh that:

Takes one argument
If the argument is "hack", output "the planet"
If the argument is "pwn", output "college"
If the argument is "learn", output "linux"
For any other input, output "unknown"


## My solve
**Flag:** `pwn.college{IyuhNOGuqHAyB0XkGWmaZIQCXcw.0FOzMDOxwiM1kjNzEzW}`

As the challenge suggest I did the same thing as earlier but in the script added the conditionals needed and got the flag.

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
