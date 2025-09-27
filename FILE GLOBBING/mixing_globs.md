# Mixing globs
In this challenge there are a few happy, but diversely-named files in /challenge/files. we have to cd there and, using the globbing we've learned, we have to write a single, short (6 characters or less) glob that (when passed as an argument to /challenge/run) will match the files "challenging", "educational", and "pwning".

## My solve
**Flag:** `pwn.college{Yyi_-9lELpKevNretEV0J3HIHVj.QX1IDO0wiM1kjNzEzW}`

As given in the challenge i first entered /challenge/files then i started using echo where i first used [hdp]* and got delightful happy pwning
so i got the idea then i used [pce]* as these are the unique letters.

```
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ echo look: [hdp]*
look: delightful happy pwning
hacker@globbing~mixing-globs:/challenge/files$ echo look: [pce]*
look: challenging educational pwning
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [pce]*
You got it! Here is your flag!
pwn.college{Yyi_-9lELpKevNretEV0J3HIHVj.QX1IDO0wiM1kjNzEzW}

```

## What I learned

Learned nothing new but learned how to use all the commands learned previously.

## References 
None.
