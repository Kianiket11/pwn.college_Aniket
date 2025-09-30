# Deleting newlines


## My solve
**Flag:** `pwn.college{EAeF6w-HmE-7IYKLT2915mWTcf7.0VNxEzNxwiM1kjNzEzW}`


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


## References 
None.
