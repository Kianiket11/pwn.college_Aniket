# Writing to multiple programs

In this challenge we need to run the /challenge/hack command, and duplicate its output as input to both the /challenge/the and 
the /challenge/planet commands. 

## My solve
**Flag:** `pwn.college{00L9r1sO_aBpZ1EXZG1KfY3pY4S.QXwgDN1wiM1kjNzEzW}`

As given in the challenge we need to duplicate the output of /challenge/hack as input to both /challenge/the and /challenge/planet, 
similar to what I did in previous challenges I used the tee command to complete the challenge and get the flag.
 
```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
1341622229180713282
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{00L9r1sO_aBpZ1EXZG1KfY3pY4S.QXwgDN1wiM1kjNzEzW}
```

## What I learned

I learnt the pipe and tee commands in more depth with this challenge.

## References 
None.
