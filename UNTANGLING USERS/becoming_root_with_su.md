# Becoming root with su 

In this challenge we need to use hack-the-planet as password, and we must provide it to su to become root!

## My solve
**Flag:** `pwn.college{gQBfUm9ZTF8lwzuBPtf5KBIQ0HB.QX1UDN1wiM1kjNzEzW}`

As given in the challenge we have to use su command with hack-the-planet as password in order to get the flag.

```
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# su
root@users~becoming-root-with-su:/home/hacker# cat flag
cat: flag: No such file or directory
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{gQBfUm9ZTF8lwzuBPtf5KBIQ0HB.QX1UDN1wiM1kjNzEzW}
```

## What I learned

I learnt about the su command which is the short form for switch users and as the name suggests it is used to switch users.

## References 
None.
