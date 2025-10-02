# Resuming processes

In this challenge we need to suspend run and resume it.

## My solve
**Flag:** `pwn.college{sODViDqQMlG8I_nRSI0jDpIsJr5.QX2QDO0wiM1kjNzEzW}`

As the challenge suggests that we need to first run /challenge/run then we cna use ctrl + z to suspend it and then we can use
fg /challenge/run to resume the process.

```
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg /challenge/run
/challenge/run
I'm back! Here's your flag:
pwn.college{sODViDqQMlG8I_nRSI0jDpIsJr5.QX2QDO0wiM1kjNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

## What I learned

I learn about the fg command which is a builin command that takes the suspended process and resumes it.

## References 
None.
