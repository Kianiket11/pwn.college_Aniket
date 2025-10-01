# Deleting newlines

In this challenge there are a bunch of newlines injected into the flag. we have to delete them.

## My solve
**Flag:** `pwn.college{EAeF6w-HmE-7IYKLT2915mWTcf7.0VNxEzNxwiM1kjNzEzW}`

As given in the challenge that there are newlines injected into the flag and we have to delete them. What we can do is use
tr -d from the previous challenge to delete with "\n" as it means new lines. Finally , we can use "flag" | tr -d "\n" in 
order to get the flag.

```
hacker@data~deleting-newlines:~$ /challenge/run
Your line-split flag: 
p
wn
.
col
le
g
e
{
E
A
e
F6w
-H
mE
-
7I
YK
L
T
2
9
15
mW
Tcf7
.
0
VNx
E
z
Nx
wi
M1k
jNz
E
zW}

hacker@data~deleting-newlines:~$ echo "p
wn
.
col
le
g
e
{
E
A
e
F6w
-H
mE
-
7I
YK
L
T
2
9
15
mW
Tcf7
.
0
VNx
E
z
Nx
wi
M1k
jNz
E
zW}
" | tr -d "\n"
pwn.college{EAeF6w-HmE-7IYKLT2915mWTcf7.0VNxEzNxwiM1kjNzEzW}
```

## What I learned

I learnt that \n is a standin for this newline, and it must be used in  quotes to prevent the shell interpreter itself 
from trying to interpret it.

## References 
None.
