# Home Sweet Home
In this challenge, /challenge/run will write a copy of the flag to any file we specify as an argument on the commandline, with these constraints:
1.Your argument must be an absolute path.
2.The path must be inside your home directory.
3.Before expansion, your argument must be three characters or less.

## My solve
**Flag:** `pwn.college{cDUswZgDdzFe7e2zXBKOJqTSsH_.QXzMDO0wiM1kjNzEzW}`

In this challenge we had to make a file and then specify it as an argument. So at first i tried /challenge/run ~/abc. Now i thoought that
my solution is satisfying all the three conditions it is an absolute path, the path is inside my home directory and the wrong parth was 
that i thought ~/abc are three characters whereas these are 5 charaters. Therefore, i corrected my mistake and ran ~/a which gave me the flag.

```
hacker@paths~home-sweet-home:~$ /challenge/run ~/abc
The argument you provided must not have been longer than 3 characters (it's 
currently 5 characters long)!
hacker@paths~home-sweet-home:~$ /challenge/run ./x
The argument you provided is not an absolute path!
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{cDUswZgDdzFe7e2zXBKOJqTSsH_.QXzMDO0wiM1kjNzEzW}

```

## What I learned
I learnt that ~$ is the shorthand for /home/hacker and that bash provides and uses this shorthand because most of our time will 
be spent inside the  home directory. I also learnt that ~ is an absolute path, and only the leading ~ is expanded. Also learnt a 
fact that cd uses our home directory as default location.

## References 
Add any references or videos u used while solving the challenge.
