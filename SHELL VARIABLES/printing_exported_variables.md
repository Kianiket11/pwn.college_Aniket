# Printing exported variables

In this challenge we need to use the env command and search for the flag.

## My solve
**Flag:** `pwn.college{kg4nwVJS1O0K-qclkoGSsAfMpFe.QX4UTN0wiM1kjNzEzW}`

As given in the challege first we use the env command and then we can easily search for our flag.

```
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=173e66c460247b555b72c3c1c483a9e06fb7fc87dae744841cc842e51b39c35b
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{kg4nwVJS1O0K-qclkoGSsAfMpFe.QX4UTN0wiM1kjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env

```

## What I learned

I learnt about the env command and how it prints out every exported variable set in our shell.

## References 
None.
