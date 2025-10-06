# Executable files

In this challenge we need to make /challenge/run executable in order to get the flag.

## My solve
**Flag:** `pwn.college{wyEpJURYfDyLx4Wraos-tabLwke.QXyEjN0wiM1kjNzEzW}`

As given in the challenge that we need to make /challenge/run executable. We can do this by using the chmod command with u+x which will make 
/challenge/run executable. But what happend was i used go-u+x which removes whatever permissions the owner currently has from group/others,
Then adds execute permission to everyone. But we didn't wanted that so i finally used u+x which adds execute (x) only to the file owner (u). 
It leaves group and others unchanged. 

```
hacker@permissions~executable-files:~$ chmod go-u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
bash: /challenge/run: Permission denied
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{wyEpJURYfDyLx4Wraos-tabLwke.QXyEjN0wiM1kjNzEzW}
```

## What I learned

I learnt how the various arguments are used with the chmod command for eg:
u+r  adds read access to the user's permissions
g+wx adds write and execute access to the group's permissions
o-w removes write access for other users
a-rwx removes all permissions for the user, group, and world

## References 
None.
