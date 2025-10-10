# Scripting with conditionals

In this challenge we need to write a script at /home/hacker/solve.sh that:

Takes one argument
If the argument is "pwn", output "college"
For any other input, output nothing

## My solve
**Flag:** `pwn.college{Ap63BaoDxIHxWn8-OYmZpl5tdRa.0lNzMDOxwiM1kjNzEzW}`

As given in the challenge we need to write a script at /home/hacker/solve.sh. So, i first deleted what we wrote earlier
and then in the script wrote the conditions provided and finally got the flag.

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

I learnt that we can use conditional such as if and else in script.

## References 
None.
