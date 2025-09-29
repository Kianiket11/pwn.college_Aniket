# Grepping stored results

In this challenge we need to follow the following steps:

1.Redirect the output of /challenge/run to /tmp/data.txt.
2.This will result in a hundred thousand lines of text, with one of them being the flag, in /tmp/data.txt.
3. grep that for the flag!

## My solve
**Flag:** `pwn.college{ooY2gvoS-C0O8xZnn-123mf7Omy.QX4EDO0wiM1kjNzEzW}
`
As the challenge suggested first i redirected the output of /challenge/run to /tmp/data.txt.then i just used the grep command 
with pwn.college to differentiate and find the flag.

```
hacker@piping~grepping-stored-results:~$ /challenge/run stdout > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{ooY2gvoS-C0O8xZnn-123mf7Omy.QX4EDO0wiM1kjNzEzW}

```

## What I learned

It was a practice problem so learnt nothing new but got reminded of the previously learnt concepts .

## References 
None.
