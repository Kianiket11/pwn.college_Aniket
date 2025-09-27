# Searching manuals
In this challenge we have to search the manual to find the flag with different options in manual page such as arrow keys (and PgUp/PgDn) and search with /.
we can also use n to go to the next result and N to go to the previous result.

## My solve
**Flag:** `pwn.college{MYecSp6Wp9_qMPrDS3RtSHPu1-d.QX1EDO0wiM1kjNzEzW}`
As the challenge suggests, we can use arrow keys (and PgUp/PgDn) and search can search with / in a manual.So, firstly i opened the manual of challenge and then
i used /flag to search for the flag there i found --fvqxae (This argument will give you the flag), Therefore, i used this command to get the flag.

```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ --fvqxae
              This argument will give you the flag
bash: --fvqxae: command not found
bash: This: command not found
hacker@man~searching-manuals:~$ /challenge/challenge --fvqxae
Initializing...
Correct usage! Your flag: pwn.college{MYecSp6Wp9_qMPrDS3RtSHPu1-d.QX1EDO0wiM1kjNzEzW}

```

## What I learned
I learnt how we can go up and down the manual and how we can use / to search a particular word in a manual.

## References 
None.

