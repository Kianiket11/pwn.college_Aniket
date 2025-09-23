# Position thy self
This challenge asks us to execute the /challenge/run program from a specific path(which a certain directory which it will tell us.
And we'll have to cd the directory to find the path.

## My solve
**Flag:** `pwn.college{AzQAWb59qnLXfyvqBPmNNUQaJo8.QX2QTN0wiM1kjNzEzW}`

For solving this challenge i had to use cd which is a command for changing directories. Now as it was mentioned that to find
the flag we had to fisrt find the specific path from which we had to invoke /challenge/run. So i started using cd to change to 
different directories and find the path. At first i go confused but then i started from the basic directory which is the home directory.
And found the path which was required to find the flag.

```
hacker@paths~position-thy-self:~$ cd /challenge
hacker@paths~position-thy-self:/challenge$ /run
bash: /run: Is a directory
hacker@paths~position-thy-self:/challenge$ cd /run
hacker@paths~position-thy-self:/run$ cd /home
hacker@paths~position-thy-self:/home$ /challenge/run
Incorrect...
You are not currently in the /sys directory.       //here the path was given which is /sys
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:/home$ cd
hacker@paths~position-thy-self:~$ cd /sys
hacker@paths~position-thy-self:/sys$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{AzQAWb59qnLXfyvqBPmNNUQaJo8.QX2QTN0wiM1kjNzEzW}
```

## What I learned
I learnt about the cd command and how useful it is while changing the directories and files in linux, and how i can use the cd command 
to navigate through different directories. I also learnt what the (~) was in the prompt. It shows the current path that your shell is located at.

## References 
None
