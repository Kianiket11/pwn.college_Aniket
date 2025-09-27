# Matching with ?

In this challenge we have to start from our home directory, change our directory to /challenge, but use the ? character 
instead of c and l in the argument to cd. 

## My solve
**Flag:** `pwn.college{8cTmNCvr2IyMUakx_4uBk9D5Axd.QXyIDO0wiM1kjNzEzW}`

As given in the challenge we just have to use ? in place of c and l while writing the argument.Therfore, doing this results 
in the change of directory. Finally i ran  /challenge/run to get the flag.

```
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8cTmNCvr2IyMUakx_4uBk9D5Axd.QXyIDO0wiM1kjNzEzW}
```

## What I learned
I learnt about the next glob which is ?. I learnt that When the shell encounters a ? character in any argument, the shell treats it 
as a single-character wildcard. Therefoere, the only difference between the two is ? works like *, but only matches one character.

## References 
None.
