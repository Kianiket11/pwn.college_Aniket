# Scripting with default cases 

In this challenge we need to write a script at /home/hacker/solve.sh that:

Takes one argument
If the argument is "pwn", output "college"
For any other input, output "nope"

## My solve
**Flag:** `pwn.college{IxLXBEaoA3jcXFaXIz3Jy10VgGa.01NzMDOxwiM1kjNzEzW}`

As the challenge suggest I did the same thing as earlier but in the script added the conditionals needed and got the flag.

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

I learnt how to use different conditionals in the script.

## References 
None.
