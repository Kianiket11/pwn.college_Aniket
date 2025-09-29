# Multi-word variables

In this challenge we need to set the variable PWN to COLLEGE YEAH.

## My solve
**Flag:** `pwn.college{Yc0mG8TGVX13sRYWwR09vPB8UV2.QXwYTN0wiM1kjNzEzW}`

As given in the challenge that we need to set the variable PWN to COLLEGE YEAH. We can do this by using 
PWN="COLLEGE YEAH".

```
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Yc0mG8TGVX13sRYWwR09vPB8UV2.QXwYTN0wiM1kjNzEzW}

```

## What I learned

I lerant that when the shell sees a space, it ends the variable assignment and interprets the next 
word as a command. Thats why we need to use quotes for COLLEGE YEAH.

## References 
None.
