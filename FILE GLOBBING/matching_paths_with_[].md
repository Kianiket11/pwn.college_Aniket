# Matching paths with []

In this challenge there are a bunch of files in /challenge/files. Starting from your home directory, run /challenge/run 
with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files.

## My solve
**Flag:** `pwn.college{0lmf6DpsA_dkMehLSyp4c9OaMeH.QX0IDO0wiM1kjNzEzW}`

As the challenge suggests we have to run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, 
file_a, file_s, and file_h files.Therefore, I ran /challenge/run /challenge/files file_[bash] the firsttime and and got an error that i called 
this command with more than 1 argument which i later resolved by using  /challenge/run /challenge/files/file_[bash].

```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files file_[bash]
Error: you called this command with more than 1 argument (pre-globbing)! Please 
call me with one argument.
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{0lmf6DpsA_dkMehLSyp4c9OaMeH.QX0IDO0wiM1kjNzEzW}

```

## What I learned
I learnt that globbing happens on a path basis and we can expand entire paths with your globbed arguments.

## References 
None.
