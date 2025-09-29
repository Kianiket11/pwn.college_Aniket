# Filtering with grep -v 

In this challenge we need to filter out all the lines containing "DECOY" and reveal the real flag.

## My solve
**Flag:** `pwn.college{w1IO-NEFTAr9CGY0GQYScWbPsCo.0FOxEzNxwiM1kjNzEzW}`

As the challenge suggests we need to filter out all the lines containing "DECOY" and reveal the real flag. We can do this 
by using grep -v DECOY as it all the lines that don't contain DECOY.

```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{w1IO-NEFTAr9CGY0GQYScWbPsCo.0FOxEzNxwiM1kjNzEzW}
```

## What I learned

I learnt that grep has option -v, which shows lines that do not match a pattern.

## References 
None.
