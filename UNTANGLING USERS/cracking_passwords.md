# Cracking passwords

In this challenge we will be given with a leak of /etc/shadow in /challenge/shadow-leak. We have to crack it and su to zardus, and run /challenge/run to get the flag

## My solve
**Flag:** `pwn.college{0TrpY7UyCVTZ8AR0r41Nxbz0gjp.QX3UDN1wiM1kjNzEzW}`

As given in the challenge that we are provided with a leak ok /etc/shadow.What we can use is John the ripper which is a tool 
in linux, used for password cracking. After using this tool we got "aardvark" as the password for zardus, after this i used
su to switch users to zardus. Finally, ran /challenge/run in order to get the flag.

```
hacker@users~cracking-passwords:~$ cat /challenge/shadow-leak
root:*:20182:0:99999:7:::
daemon:*:20182:0:99999:7:::
bin:*:20182:0:99999:7:::
sys:*:20182:0:99999:7:::
sync:*:20182:0:99999:7:::
games:*:20182:0:99999:7:::
man:*:20182:0:99999:7:::
lp:*:20182:0:99999:7:::
mail:*:20182:0:99999:7:::
news:*:20182:0:99999:7:::
uucp:*:20182:0:99999:7:::
proxy:*:20182:0:99999:7:::
www-data:*:20182:0:99999:7:::
backup:*:20182:0:99999:7:::
list:*:20182:0:99999:7:::
irc:*:20182:0:99999:7:::
gnats:*:20182:0:99999:7:::
nobody:*:20182:0:99999:7:::
_apt:*:20182:0:99999:7:::
systemd-timesync:*:20357:0:99999:7:::
systemd-network:*:20357:0:99999:7:::
systemd-resolve:*:20357:0:99999:7:::
mysql:!:20357:0:99999:7:::
messagebus:*:20357:0:99999:7:::
sshd:*:20357:0:99999:7:::
hacker::20357:0:99999:7:::
zardus:$6$Zl1fS96J/6Yb1v9f$3gy/iqMXTcOy2s9MZZUOYxJR/5jr9Vg8qItQ.LkOjwLLb/sxP.5pXfuKJtJSMooKIXaZRCv4JmG.K64cZ7gXL0:20361:0:99999:7:::
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:21 100% 2/3 0.04694g/s 273.3p/s 273.3c/s 273.3C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{0TrpY7UyCVTZ8AR0r41Nxbz0gjp.QX3UDN1wiM1kjNzEzW}
```

## What I learned

I learnt about how passwords are cracked and also learnt how passwords are stored as hash and how we can use John the ripper.
which is used to crack passwords.

## References 
None.
