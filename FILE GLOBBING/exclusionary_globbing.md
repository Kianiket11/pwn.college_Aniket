# Exclusionary globbing 

In this challenge we have to go forth to /challenge/files and then run /challenge/run with all files that don't start with p, w, or n.

## My solve
**Flag:** `pwn.college{ooPaAqjGgaaBZF-eAH935arNvMi.QX2IDO0wiM1kjNzEzW}`

As the challenge suggests first we have to enter /challenge/files there i used [!pwn]* with echo to check what all files are getting
displayed. then i ran /challenge/run [!pwn]* to finally get the flag.

```
hacker@globbing~exclusionary-globbing:$cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ echo look [!pwn]*
look amazing beautiful challenging delightful educational fantastic great happy incredible jovial kind laughing magical optimistic queenly radiant splendid thrilling uplifting victorious xenial youthful zesty
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{ooPaAqjGgaaBZF-eAH935arNvMi.QX2IDO0wiM1kjNzEzW}
```

## What I learned
I learnt how to filter out files in a glob using []. i also learnt that If the first character in the brackets is a ! or (in newer 
versions of bash) a ^, the glob inverts, and that bracket instance matches characters that aren't listed. 

## References 
None.
