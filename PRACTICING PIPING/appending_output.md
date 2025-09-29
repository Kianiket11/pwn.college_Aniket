# Appending output 

In this challenge we need to run /challenge/run with an append-mode redirect of the output to the file /home/hacker/the-flag. And 
the first half of the flag to the file, and the second half to stdout if stdout is redirected to the file.

## My solve
**Flag:** `pwn.college{YBM6zgdRDlNAJ-7lNBYYKuF9eaK.QX3ATO0wiM1kjNzEzW}`

As given in the challenge we need to run /challenge/run with an append-mode (>>) and redirect the output to /home/hacker/the-flag. 
can do this by using the command /challenge/run stdout >> /home/hacker/the-flag.

```
hacker@piping~appending-output:~$ /challenge/run stdout >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do 
the first write directly to the file, and the second write, I'll do to stdout 
(if it's pointing at the file). If you redirect the output in append mode, the 
second write will append to (rather than overwrite) the first write, and you'll 
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
 | 
\|/ This is the first half:
 v 
pwn.college{YBM6zgdRDlNAJ-7lNBYYKuF9eaK.QX3ATO0wiM1kjNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>) 
rather than *append* mode (>>), and so the write of the second half to stdout 
overwrote the initial write of the first half directly to the file. Try append 
mode!
```

## What I learned

I learnt that we can redirect input in append mode using >> instead of >.

## References 
None.
