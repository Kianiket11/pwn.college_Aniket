# Matching with []

In this challenge there are a bunch of files in /challenge/files. we have to change our working directory to /challenge/files 
and run /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h.

## My solve
**Flag:** `pwn.college{QwwO3B042rtEKI5zBlJp6edzxlz.QXzIDO0wiM1kjNzEzW}`

As the challenge suggests, We have to change our directories.So, I jsut used cd /challenge/files, Then as in order to find the 
flag we need to run /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h. Threfore, 
I used /challenge/run file_[bash] in order to get the flag.
```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{QwwO3B042rtEKI5zBlJp6edzxlz.QXzIDO0wiM1kjNzEzW}
```

## What I learned

I learnt about the next glob which is []. I learnt that square brackets are, essentially, a limited form of ?. As instead of matching 
any character [] is a wildcard for some subset of potential characters, specified within the brackets.

## References 
None.
