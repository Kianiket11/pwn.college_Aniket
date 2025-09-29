# Named pipes

In this challenge we need to create a /tmp/flag_fifo file and redirect the stdout of /challenge/run to it.

## My solve
**Flag:** `pwn.college{cH_kVX0aL5Hh-leIQHU0ZHvzGWB.01MzMDOxwiM1kjNzEzW}`

As given in the challenge i first created a fifo file using mkfifo then i redirected the output of /challenge/run to /tmp/flag_fifo
(fifo which we made).

```bash
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of
/challenge/run. Recall that operations on FIFOs will *block* until both the
read side and the write side is open, so /challenge/run will not actually be
launched until you start reading from the FIFO!
hacker@piping~named-pipes:~$


terminal 2


hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
pwn.college{cH_kVX0aL5Hh-leIQHU0ZHvzGWB.01MzMDOxwiM1kjNzEzW}

```

## What I learned

I learned about FIFO which stands for First In First Out. FIFO's are basically named pipes and we can create fifo's with mkfifo command.


## References 
None.
