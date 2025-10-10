# Understanding shebangs

In this challenge we need to create a script at /home/hacker/solve.sh that has a proper shebang and outputs "hack the planet". 
and we need to make it executable, then run /challenge/run to verify if the script works correctly.

## My solve
**Flag:** `pwn.college{oU0ZrJ7pdz0VXEkG-D2D7h8P243.0VOzMDOxwiM1kjNzEzW}`

As given in the challenge i created a script in /home/hacker/solve.sh using nano and later typed #!/bin/bash echo hack the planet
which is a shebang as suggested in the challenge and later did the same thing as previous challenge and got the flag.

```
hacker@chaining~understanding-shebangs:~$ nano /home/hacker/solve.sh
#!/bin/bash
echo hack the planet
hacker@chaining~understanding-shebangs:~$ ls -l solve.sh
-rw-r--r-- 1 hacker hacker 34 Oct  9 19:19 solve.sh
hacker@chaining~understanding-shebangs:~$ chmod 777 solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{oU0ZrJ7pdz0VXEkG-D2D7h8P243.0VOzMDOxwiM1kjNzEzW}
```

## What I learned

I learnt about shebang which is just a term used for program files that starts with the characters #!. 

## References 
None.
