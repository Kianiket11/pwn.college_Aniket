# Reading Input 

In this challenge we need to use read to set the PWN variable to the value COLLEGE.

## My solve
**Flag:** `pwn.college{41oU0B1mqeUtpe7Aivt7A5b4Nmt.QX4cTN0wiM1kjNzEzW}`

As the challenge suggests we can use read to set the PWN variable to the value COLLEGE. This can be done by 
read -p "INPUT: " PWN and later in the input we can write COLLEEGE which will give us the flag.

```
hacker@variables~reading-input:~$ read -p "INPUT: " PWN
INPUT: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{41oU0B1mqeUtpe7Aivt7A5b4Nmt.QX4cTN0wiM1kjNzEzW}
```

## What I learned

I learnt how we can read input from users which is done by using read command with -p as argument.

## References 
None.
