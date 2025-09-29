# Split-piping stderr and stdout

In this challenge we have /challenge/hack: this produces data on stdout and stderr and we have to redirect hack's 
stderr to /challenge/the and we have to redirect hack's stdout to /challenge/planet.

## My solve
**Flag:** `pwn.college{A8jRMltKR-uFdv8AdfEvNtWTAYM.QXxQDM2wiM1kjNzEzW}`

As given in the challenge, I redirected the stderr of /challenge/hack to /challenge/the and stdout to /challenge/planet.

```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) | /challenge/planet
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{A8jRMltKR-uFdv8AdfEvNtWTAYM.QXxQDM2wiM1kjNzEzW}
```

## What I learned

Nothing much to learn but this challenge is a good revision of the things learned in this module.

## References 
None.
