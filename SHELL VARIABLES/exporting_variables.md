# Exporting variables


## My solve
**Flag:** `pwn.college{EAB7xowEgnrQa8JSblP2_tOLM8Q.QXyYTN0wiM1kjNzEzW}`


```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ sh
sh-5.2$ /challenge/run $PWN
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{EAB7xowEgnrQa8JSblP2_tOLM8Q.QXyYTN0wiM1kjNzEzW}
```

## What I learned


## References 
None.

