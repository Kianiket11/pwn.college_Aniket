# Redirecting errors
In this challenge we need redirect the output of /challenge/run, like before, to myflag, and the "errors" to instructions.

## My solve
**Flag:** `pwn.college{s716bqnkhF6BWE-iueQnvgV2VS_.QX3YTN0wiM1kjNzEzW}`

As the challenge suggests we need to redirect the out of /challenge/run to myflag and errors(FD 2) to instructions.Therefore, 
i just used the command /challenge/run stdout > myflag 2> instructions, and latere ran cat to get the flag.

```
hacker@piping~redirecting-errors:~$ /challenge/run stdout > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{s716bqnkhF6BWE-iueQnvgV2VS_.QX3YTN0wiM1kjNzEzW}
```

## What I learned

I learnt that how we can also redirect the error channel of commands. I learnt about File Descriptor numbers.

## References 
Used this video for more knowledge of redirecting `https://www.youtube.com/watch?v=lRokPC5ZrPU`.
