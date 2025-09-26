# Moving Files
In this challenge we have to move the flag into another directory using mv command

## My solve
**Flag:** `pwn.college{c1MN5MaYLwFaDmTBE5SheLnZXBf.0VOxEzNxwiM1kjNzEzW}`

As the challenge mentiones that we have to move the /flag to /tmp/hack-the-planet.Therefore, we can just write the mv 
command to move the flag inside the given direcotry and then find the flag 

```
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{c1MN5MaYLwFaDmTBE5SheLnZXBf.0VOxEzNxwiM1kjNzEzW}
```

## What I learned
I learnt about the mv command, which is the shortform for move and as the name suggests it is used to basically move 
files from one location to another.

## References 
None.

