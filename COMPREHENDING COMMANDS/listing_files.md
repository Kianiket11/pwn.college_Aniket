# Listing Files

In this challeng the direcotry /challenge/run is named with some random name!. we have to list the files in /challenge to find it.

## My solve
**Flag:** `pwn.college{AGofh9pzbKr-AsEaWp3LgeQ0ouF.QX4IDO0wiM1kjNzEzW}`

So, as the challenge suggested that we have to find the random named file in /challenge which is our flag.Therefore, i used ls /challenge
command to list all the files in /challenge. There 3963-renamed-run-1174 was the random named file i found, therefore is used 
/challenge/3963-renamed-run-1174, To capture the flag.

```
hacker@commands~listing-files:~$ ls /challenge
3963-renamed-run-1174  DESCRIPTION.md
hacker@commands~listing-files:~$ ls /3963-renamed-run-1174
ls: cannot access '/3963-renamed-run-1174': No such file or directory
hacker@commands~listing-files:~$ /challenge/3963-renamed-run-1174
Yahaha, you found me! Here is your flag:
pwn.college{AGofh9pzbKr-AsEaWp3LgeQ0ouF.QX4IDO0wiM1kjNzEzW}

```

## What I learned

I learnt about the ls command which is used to list files in all the directories provided to it as arguments, and 
in the current directory if no arguments are provided. ls is shortform for list.

## References 
None.

