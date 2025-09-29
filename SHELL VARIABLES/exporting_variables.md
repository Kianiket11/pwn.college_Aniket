# Exporting variables

In this challenge we need to invoke /challenge/run with the PWN variable exported and set to the value 
COLLEGE, and the COLLEGE variable set to the value PWN but not exported.

## My solve
**Flag:** `pwn.college{EAB7xowEgnrQa8JSblP2_tOLM8Q.QXyYTN0wiM1kjNzEzW}`

As the challenge suggests first we need to set and export variable PWN to COLLEGE and then we need to set COLLEGE to PWN,
but not export it. And Finally we can invoke /challenge/run with PWN in order to get the flag.

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

I learnt about the sh command and why its called child of the main shell. Then i learnt about exporting and how its done 
using the export command.

## References 
None.

