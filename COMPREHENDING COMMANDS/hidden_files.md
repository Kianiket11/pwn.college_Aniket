# Hidden Files 

In this challenge we have to search for the hidden file in the root(/) directory, hidden as a dot-prepended file.

## My solve
**Flag:** `pwn.college{IgvxutxbbyURskK1lpHJSEghrwk.QXwUDO0wiM1kjNzEzW}`

As the flag is hidden in the root directory,  we first enter the root directory using cd and then as it is given that 
the hidden file is dot-prepended, therefore we'll have to use ls -a to list the dot-prepended files. Finally, we can 
use the cat command to get the flag.


```
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-24639316828613  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-24639316828613
pwn.college{IgvxutxbbyURskK1lpHJSEghrwk.QXwUDO0wiM1kjNzEzW}
hacker@commands~hidden-files:/$ 

```

## What I learned

I learnt that when we use ls it doesn't show us all the files and that many files that are dot-prepended are hidden. I learnt that
we can use -a with ls (ls -a) to list the dot-prepended hidden files.

## References 
None.

