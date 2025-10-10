# Scripting with arguments

In this challenge we need to write a script at /home/hacker/solve.sh that:
 # Takes two arguments
 # Outputs them in REVERSE order (second argument first, then the first argument)

## My solve
**Flag:** `pwn.college{EzFEQyejWdI-m9X9wKLwVPatfut.0VNzMDOxwiM1kjNzEzW}`

As given in the challenge that we need to write a script at /home/hacker/solve.sh. So, i first deleted what was written 
earlier in the script and added #!/bin/bash echo $2 $1 which satisfies both the conditions given in the challenge and 
we finally got the flag.

```
hacker@chaining~scripting-with-arguments:~$ nano /home/hacker/solve.sh
#!/bin/bash
echo $2 $1
hacker@chaining~scripting-with-arguments:~$ ./solve.sh pwn college
college pwn
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{EzFEQyejWdI-m9X9wKLwVPatfut.0VNzMDOxwiM1kjNzEzW}
```

## What I learned

I learnt that the script can access these arguments using special variables:

$1 contains the first argument ("hello")
$2 contains the second argument ("world")
$3 would contain the third argument (if there had been one) ...

## References 
None.
