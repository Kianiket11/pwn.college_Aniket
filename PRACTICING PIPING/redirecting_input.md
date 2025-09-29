# Redirecting input

In this challenge we need to redirect the PWN file to /challenge/run and have the PWN file contain the value COLLEGE.

## My solve
**Flag:** `pwn.college{k7Se9myUw9ijeGfjvAc9HBAJ4Dv.QXwcTN0wiM1kjNzEzW}`

As given in the challenge firstly we need the PWN file to containg COLLEGE to do so we can use echo COLLEGE > PWN. Next we can use
/challenge/run rev < PWN to redirect the PWN file. 

```
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run rev < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{k7Se9myUw9ijeGfjvAc9HBAJ4Dv.QXwcTN0wiM1kjNzEzW}
```

## What I learned

I learnt how we can redirect input using (<).

## References 
None.
