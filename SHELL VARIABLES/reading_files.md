# Reading Files

In this challenge we need to read /challenge/read_me into the PWN environment variable.

## My solve
**Flag:** `pwn.college{kYn2xbf-t3VKmUTS6uN4DTLbz68.QXwIDO0wiM1kjNzEzW}`

As the challenge suggests I used the read command to complete the challenge.

```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{kYn2xbf-t3VKmUTS6uN4DTLbz68.QXwIDO0wiM1kjNzEzW}
```

## What I learned

I learnt that we can also read files using shell with the read command.

## References 
None.
