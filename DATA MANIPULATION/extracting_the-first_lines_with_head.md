# Extracting the first lines with head

In this challenege /challenge/pwn outputs a bunch of data, and you'll need to pipe it through head to grab 
just the first 7 lines and then pipe them onwards to /challenge/college.

## My solve
**Flag:** `pwn.college{IidDRzJiuvmZvavYGYxfSDbOW6C.0lNxEzNxwiM1kjNzEzW}`

As the challenge suggests first we need to pipe the data through head and then grap the first 7 lines and then pipe it again towards
/challenge/college. Firstly i used cat with /challenge/pwn and got error because /challenge/pwn is already giving use a lot 
of data as the output. Therefore, we don't need cat we can jus use /challenge/pwn | head now as we need only the first 7 lines we'll use
-n 7. Finally we will use the pipe command from previous modules to pipe the data to /challenge/college in order to get the flag.

```
hacker@data~extracting-the-first-lines-with-head:~$ cat /challenge/pwn | head -n 7 | /challenge/college
Invalid codes!
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{IidDRzJiuvmZvavYGYxfSDbOW6C.0lNxEzNxwiM1kjNzEzW}
```

## What I learned

I learnt about he head command, I learnt that the head command is used to display the first few lines of its input and 
by default it gives us the first 10 lines of input but we can control it with -n option.

## References 
None.
