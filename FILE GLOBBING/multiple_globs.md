# Multiple globs

In this challenge there are a few happy,but diversely-named files in /challenge/files. we have to cd there and run /challenge/run, providing 
a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p.

## My solve
**Flag:** `pwn.college{8nx9ed3DbGxGhuQWhiRdhQlG3hZ.0lM3kjNxwiM1kjNzEzW}`

As the challenge suggests that first we need to go to the /challenge/files using cd. after reaching i used /challenge/run *p* in order 
to obtain the flag.

```
hacker@globbing~multiple-globs:/opt$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ ls
amazing    challenging  educational  great  incredible  kind      magical  optimistic  queenly  splendid   uplifting   wonderful  youthful
beautiful  delightful   fantastic    happy  jovial      laughing  nice     pwning      radiant  thrilling  victorious  xenial     zesty
hacker@globbing~multiple-globs:/challenge/files$ cat /challenge/run/*p*
cat: '/challenge/run/*p*': Not a directory
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{8nx9ed3DbGxGhuQWhiRdhQlG3hZ.0lM3kjNxwiM1kjNzEzW}
```

## What I learned
I learnt that Bash supports the expansion of multiple globs in a single word.

## References 
None.
