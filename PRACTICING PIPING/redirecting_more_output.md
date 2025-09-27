# Redirecting more outputs

In this challenge, /challenge/run will once more give us the flag, but we have to redirect its output to the file myflag.

## My solve
**Flag:** `pwn.college{4dLbN3NW0YYz9V1rzDtk2ARQ2uc.QX1YTN0wiM1kjNzEzW}`

As the challenge suggests, we have to redirect the output of /challenge/run to a file named myflag.

```
hacker@piping~redirecting-more-output:~$ /challenge/run my stdout > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{4dLbN3NW0YYz9V1rzDtk2ARQ2uc.QX1YTN0wiM1kjNzEzW}
```

## What I learned

I learnt that aside from redirecting the output of echo, we can also redirect the output of any command.

## References 
None.
