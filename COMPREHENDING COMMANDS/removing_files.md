# Removing Files

In this challenge there's a delete_me file created in our home directory we have to delete it to get the flag.

## My solve
**Flag:** `pwn.college{0LParZOMlevI64Jm8aU0S9jSjTN.QX2kDM1wiM1kjNzEzW}`

Challenge is pretty simple here as the it is already given that the delete_me file is in the home directory we just have
to use the rm command to delete the file and get the flag.

```
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{0LParZOMlevI64Jm8aU0S9jSjTN.QX2kDM1wiM1kjNzEzW}

```

## What I learned

I learnt about the rm command which is the shortform for remove and as the name suggests this command is used to remove/delete
files.

## References 
None.

