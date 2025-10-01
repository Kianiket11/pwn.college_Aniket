# Translating characters

In this challenge /challenge/run will print the flag but will swap the casing of all characters such that A becomes a and vice-versa.

## My solve
**Flag:** `pwn.college{wjHkdMXXuLF7WKiPBu3AmXSYn2e.01MxEzNxwiM1kjNzEzW}`

As given in the challlenge /challenge/run gave us the case swapped flag now i used tr command which can be used for replacing the case
-swapped letter with the original one. What we have to do is replace "A-Z" with "a-z" and "a-z" with "A-Z" and we have to do this 
simultaneously in order to get the flag.

```
hacker@data~translating-characters:~$ /challenge/run
Your case-swapped flag:
PWN.COLLEGE{WJhKDmxxUlf7wkIpbU3aMxsyN2E.01mXeZnXWIm1KJnZeZw}
hacker@data~translating-characters:~$ echo PWN.COLLEGE{WJhKDmxxUlf7wkIpbU3aMxsyN2E.01mXeZnXWIm1KJnZeZw} | tr ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
pwn.college{wjHkdMXXuLF7WKiPBu3AmXSYn2e.01MxEzNxwiM1kjNzEzW}
```

## What I learned

I learnt about the tr command which is short form for translates and it basically translates characters it receives over standard 
input and prints them to standard output.

## References 
None.
