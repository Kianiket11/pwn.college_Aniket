# Touching Files

In this challenge we have to create two files pwn and college in the tmp directory to get the flag.

## My solve
**Flag:** `pwn.college{k-ty6gAP_dmY78Cif774V-6q9Wx.QXwMDO0wiM1kjNzEzW}`

As the challenge suggests that we have to create two files in the tmp directory, therefore first we have to enter the tmp directory
and then we'll use the touch command to create our first file pwn and then again we'll use the same command to create the college
file. After this we can use ls to check whether what we did was correct or not.

```
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{k-ty6gAP_dmY78Cif774V-6q9Wx.QXwMDO0wiM1kjNzEzW}
```

## What I learned

I learnt about the touch command, which is basically used to create files.

## References 
None.

