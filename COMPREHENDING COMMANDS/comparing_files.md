# Comparing files
In this challenge There are two files in /challenge, Both of them containing 100 fake flags each but the one file
contains 99 fake flags and 1 real flag. we have to find the flag using diff command.



## My solve
**Flag:** `pwn.college{0m5H6p3-ScBAx_EMufE1S2qvPeR.01MwMDOxwiM1kjNzEzW}`

In this challenge we knew that  /challenge/decoys_only.txt contains 100 fake flags and 
/challenge/decoys_only.txt /challenge/decoys_and_real.txt coantins 99 fake flags but 1 real flag. Therefore, we can use the 
diff command as we have to find that one different flag. 

```
hacker@commands~comparing-files:~$ cat /challenge/decoys_only.txt
//100 flags mentioned
hacker@commands~comparing-files:~$ cat /challenge/decoys_and_real.txt
//100 flags mentioned
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt 
67a68
> pwn.college{0m5H6p3-ScBAx_EMufE1S2qvPeR.01MwMDOxwiM1kjNzEzW}

```

## What I learned

I learnt about the diff command which is a very efficient command when looking for changes between similar files. diff compares two files line by line and shows you exactly what's different between them. I also learnt the two types of output we get while using diff,  which are 
XcYand XaY, here X and Y can be any line of the file. XcY tells us the difference between the two files. but XaY tells us that after the 
line X of the file line Y was added in the second file. The similar out we got in our challenge 67a68 this means that after the 67th line of 
the first file a new line was added in 68th line of 2nd file, Indicating that this the different flag.

## References 
None.

