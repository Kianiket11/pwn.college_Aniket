# Catting Absolute Paths

In this challenge the flag in not in our home directory, and we have to read it with cat at its absolute path: /flag.

## My solve
**Flag:** `pwn.college{ssTAEf2GcKjsU2UrV0TEw8_KQlR.QX5ETO0wiM1kjNzEzW}`

As the challenge states that this time the flag is not in our home directory but rather in root directory(/).Therefore we 
have to read that flag from /flag directory by using the command cat /flag.

```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{ssTAEf2GcKjsU2UrV0TEw8_KQlR.QX5ETO0wiM1kjNzEzW}
```

## What I learned
I learnt that we can specify cat's arguments as absolute paths like we did in this challenge.

## References 
None.

