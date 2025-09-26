# An epic filesytem quest

In this challenge we have to use our knowledge of previous modules and practice problems to find the flag using given
clues :
0.Your first clue is in /. Head on over there.
1.Look around with ls. There'll be a file named HINT or CLUE or something along those lines!
2.cat that file to read the clue!
3.Depending on what the clue says, head on over to the next directory (or don't!).
4.Follow the clues to the flag!

## My solve
**Flag:** `pwn.college{0pqzMTjltRNZkS42A-LXJR9a3GW.QX5IDO0wiM1kjNzEzW}`

To solve this challenge we'll just be using the clues in order. First clue was that it all starts in the root directory.
So, we enter the root directory and there we see the 'MEMO' file we use cat to read it and the second clue was '"Watch out! 
The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct".
Now as we cannot use cd to find the flag we can use to go into the given directory which is /opt/linux/linux-5.4/include/linux/mfd/mt6397.
After entering we find our thirst clue which was a file name "ALERT-TRAPPED", now as we cannot use cd we just use cat with the 
absolute path of the file and we get our next clue. And now we just have to be patient and repeat the process to capture the flag.


```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
MEMO  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin   challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat MEMO
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/include/linux/mfd/mt6397

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/include/linux/mfd/mt6397
cat: /opt/linux/linux-5.4/include/linux/mfd/mt6397: Is a directory
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/include/linux/mfd/mt6397
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/linux/mfd/mt6397$ ls
ALERT-TRAPPED  core.h  registers.h
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/include/linux/mfd/mt6397/ALERT-TRAPPED
Great sleuthing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/importlib_resources/tests/__pycache__
The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/local/lib/python3.8/dist-packages/importlib_resources/tests/__pycache__
cat: /usr/local/lib/python3.8/dist-packages/importlib_resources/tests/__pycache__: Is a directory
hacker@commands~an-epic-filesystem-quest:/$ cat __pycache__
cat: __pycache__: No such file or directory
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/local/lib/python3.8/dist-packages/importlib_resources/tests/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/importlib_resources/tests/__pycache__$ ls
DOSSIER                                 test_contents.cpython-38.pyc    test_open.cpython-38.pyc    test_resource.cpython-38.pyc
__init__.cpython-38.pyc                 test_custom.cpython-38.pyc      test_path.cpython-38.pyc    util.cpython-38.pyc
_path.cpython-38.pyc                    test_files.cpython-38.pyc       test_read.cpython-38.pyc    zip.cpython-38.pyc
test_compatibilty_files.cpython-38.pyc  test_functional.cpython-38.pyc  test_reader.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/importlib_resources/tests/__pycache__$ cat DOSSIER
Great sleuthing!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/feature/ps/unusual

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/importlib_resources/tests/__pycache__$ cd /opt/busybox/busybox-1.33.2/include/config/feature/ps/unusual
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/ps/unusual$ ls
systems.h
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/ps/unusual$ ls -a
.  ..  .REVELATION  systems.h
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/ps/unusual$ cat .REVELATION 
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/sympy/matrices/__pycache__
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/ps/unusual$ cd /usr/local/lib/python3.8/dist-packages/sympy/matrices/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/matrices/__pycache__$ ls
GIST                           eigen.cpython-38.pyc       matrices.cpython-38.pyc     sparse.cpython-38.pyc
__init__.cpython-38.pyc        exceptions.cpython-38.pyc  matrixbase.cpython-38.pyc   sparsetools.cpython-38.pyc
common.cpython-38.pyc          graph.cpython-38.pyc       normalforms.cpython-38.pyc  subspaces.cpython-38.pyc
decompositions.cpython-38.pyc  immutable.cpython-38.pyc   reductions.cpython-38.pyc   utilities.cpython-38.pyc
dense.cpython-38.pyc           inverse.cpython-38.pyc     repmatrix.cpython-38.pyc
determinant.cpython-38.pyc     kind.cpython-38.pyc        solvers.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/matrices/__pycache__$ cat GIST
Lucky listing!
The next clue is in: /var/lib/systemd/deb-systemd-helper-enabled/timers.target.wants
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/sympy/matrices/__pycache__$ cd /var/lib/systemd/deb-systemd-helper-enabled/timers.target.wants
hacker@commands~an-epic-filesystem-quest:/var/lib/systemd/deb-systemd-helper-enabled/timers.target.wants$ ls
TEASER                   apt-daily.timer    fstrim.timer  motd-news.timer
apt-daily-upgrade.timer  e2scrub_all.timer  man-db.timer  phpsessionclean.timer
hacker@commands~an-epic-filesystem-quest:/var/lib/systemd/deb-systemd-helper-enabled/timers.target.wants$ cat TEASER
Tubular find!
The next clue is in: /opt/linux/linux-5.4/arch/arm/plat-orion/include

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/var/lib/systemd/deb-systemd-helper-enabled/timers.target.wants$ cd /opt/linux/linux-5.4/arch/arm/plat-orion/include
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/arm/plat-orion/include$ ls -a
.  ..  .SECRET  plat
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/arm/plat-orion/include$ cat .SECRET 
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/drivers/net/ethernet/ibm

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/arm/plat-orion/include$ cd /opt/linux/linux-5.4/drivers/net/ethernet/ibm
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/net/ethernet/ibm$ ls -a
.  ..  .INFO  Kconfig  Makefile  ehea  emac  ibmveth.c  ibmveth.h  ibmvnic.c  ibmvnic.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/net/ethernet/ibm$ cat .INFO
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/arch/mips/crypto

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/net/ethernet/ibm$ cd /opt/linux/linux-5.4/arch/mips/crypto
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/mips/crypto$ ls -a
.  ..  .DISPATCH  Makefile  crc32-mips.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/mips/crypto$ cat .DISPATCH 
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{0pqzMTjltRNZkS42A-LXJR9a3GW.QX5IDO0wiM1kjNzEzW}
```

## What I learned

There was no technical learning in this challenge as we just had to use what we learnt earlier, The important learning was that 
we should be confident with what we are doing as in this challenge we had to repeat the process, I though maybe i was doing something 
wrong and was thinking of quitting the challenge as i never solved a challenge that took this long.


## References 
None.

