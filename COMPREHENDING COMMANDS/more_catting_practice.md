# More cattting practice
In this challenge we have to find the flag from the directory without using cd to reach that directory.

## My solve
**Flag:** `pwn.college{8lUhkKAhV0wsIaY8qFO2N13dt6L.QXwITO0wiM1kjNzEzW}`

In this challenge the path was clearly meantioned to us as /usr/include/netash/flag, Therefore we just had to use 
cat /usr/include/netash/flag to find the flag as we learnt earlier that we can specify absolute paths in cat.

```bash
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /usr/include/netash/flag. Go cat it out **without** cding into that 
directory!

hacker@commands~more-catting-practice:~$ cat /usr/include/netash/flag
pwn.college{8lUhkKAhV0wsIaY8qFO2N13dt6L.QXwITO0wiM1kjNzEzW}
```

## What I learned
Noting much to learn as this is just for practicing what we have learnt in the previous challenge.

## References 
None.

