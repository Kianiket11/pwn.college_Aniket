# Grepping Errors

In this challenge we need to redirect standard error to standard output (2>& 1) and then pipe the now-combined stderr 
and stdout as normal.

## My solve
**Flag:** `pwn.college{sSM0WduD7Qts-8GaOsuhlgjJqSl.QX1ATO0wiM1kjNzEzW}`

As given in the challenge firstly we need to redirect standard error to standard output therefore, i used /challenge/run 2>& 1 to do so
and used | grep pwn.college to get the flag.

```
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{sSM0WduD7Qts-8GaOsuhlgjJqSl.QX1ATO0wiM1kjNzEzW}
```

## What I learned

I leanrnt that the shell has a (>&) operator, which redirects a file descriptor to another file descriptor. 

## References 
None.
