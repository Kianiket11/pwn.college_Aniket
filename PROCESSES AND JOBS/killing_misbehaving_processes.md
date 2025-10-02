# Killing misbehaving processes

In this challenge there's a decoy process that's hogging a critical resource - a named pipe (FIFO) at /tmp/flag_fifo 
into which  /challenge/run wants to write your flag. We need to kill this process.

## My solve
**Flag:** `pwn.college{AKk2aG8Z4iS4zv67UWhmvpVxf8H.0FNzMDOxwiM1kjNzEzW}`

As given in the challenge first we need to see all the processes running. There we can see that the PID 142 is /challenge/decoy
so we use kill 142 to kill the process. Next i used /challenge/run which will write the flag to the FIFO. Then i used cat /tmp/flag_fifo
in order to list all the flag including the decoys. Then again I ran /challenge/run so that it will write the real flag into 
/tmp/flag_fifo and finally we can just cat the file.

```
hacker@processes~killing-misbehaving-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.3  0.0   1056   640 ?        Ss   03:58   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo
root           7  0.2  0.0 231708  2560 ?        S    03:58   0:00 /run/dojo/bin/sleep 6h
root         137  0.0  0.0   4132   960 ?        S    03:58   0:00 /bin/bash /challenge/.init
root         138  0.0  0.0   4132  1280 ?        S    03:58   0:00 /bin/bash /challenge/.init
root         139  0.0  0.0   5204  3520 ?        S    03:58   0:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140  0.0  0.0   2744  1600 ?        S    03:58   0:00 sleep 6h
root         141  0.0  0.0   2744  1600 ?        S    03:58   0:00 sleep 6h
hacker       142  0.3  0.0  13516  9280 ?        Ss   03:58   0:00 /usr/bin/python /challenge/decoy
hacker       154  0.2  0.0  36972 22080 ?        Sl   03:58   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --
hacker       158  0.0  0.0 231972  4160 pts/0    Ss   03:58   0:00 /run/dojo/bin/bash --login
hacker       168  0.0  0.0 233600  3840 pts/0    R+   03:58   0:00 ps aux
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.1  0.0   1056   640 ?        Ss   03:58   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo
root           7  0.1  0.0 231708  2560 ?        S    03:58   0:00 /run/dojo/bin/sleep 6h
root         137  0.0  0.0   4132   960 ?        S    03:58   0:00 /bin/bash /challenge/.init
root         138  0.0  0.0   4132  1280 ?        S    03:58   0:00 /bin/bash /challenge/.init
root         140  0.0  0.0   2744  1600 ?        S    03:58   0:00 sleep 6h
root         141  0.0  0.0   2744  1600 ?        S    03:58   0:00 sleep 6h
hacker       154  0.0  0.0  36972 22080 ?        Sl   03:58   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --
hacker       158  0.0  0.0 231972  4160 pts/0    Ss   03:58   0:00 /run/dojo/bin/bash --login
hacker       169  0.0  0.0 233600  3840 pts/0    R+   03:58   0:00 ps aux
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
^C
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{gg.m0wgvc5tX-GmBnrJBtrULTc9MB4ysRnZEQA0j6FCSpg5}
pwn.college{mAzpDxrxlpIvv7wAeS-zvq60S9ZN2SESaiPDw7xf4SdJIg.}
pwn.college{E1PsxdaVGri5Qy47nwYnCJ8M0cokMwjpx3wRKBmcKVGgBHA}
pwn.college{TgFIzILrC.dRODgRH3Cx0ueOZ7ykac74oKjBKnwVB4hoaxO}
pwn.college{W4KUFHNRMGOT2hhXq4XsjHB.wiIe-4-vZzVGprs3qzHM8pF}
pwn.college{6BzhhmFNEZIPZrugnkxrCYmyEaleKAxOHDWFvVDoopTDk-z}
pwn.college{phF-r1DP3tR.wUeBnPE-vmTmoLk4Q88Xqu3led73pJ5Qx9P}
pwn.college{NUEQFWB6y2XS9SnjPClViOBSYsvDV-Og6wlCRbbSEAoAyua}
pwn.college{Hhb5L9VKyRLbzq4JawYn6NyAMnHPCi1gFSazxn.ENdoTx3o}
pwn.college{CbU68EZ9AxPQlYeV00vakiV7NSfQdeYP2-0wvSiXDMci8fq}
pwn.college{tti8lMFR00hlz6xFFEGpwiWseVjlyJ5vyT4BGRqM4hEJYYT}
pwn.college{th.FOLLdZV6ZKApYqoHmcTwpZ9RKlSDIpFSDtcpHiAwzU1U}
pwn.college{2jqMoQpA-FmtIHeMg.GkK3OS.dVCDTumJY8YtR7WNH7qm5n}
pwn.college{wUSvcCdaQjVDs6ZGtqFQBTZAiEH5tWg6rVHjHlHnYLrRJv8}
pwn.college{KQU08BgZvC6xcubzWnlhZKDLNo6tfNmAetvEOLdZDSTfnHH}
pwn.college{VXdOkDlWlH0IB3R0CZCfgBqlXCnva4t1QZcI1QJ3x8l7C6g}
pwn.college{9GoieIgps57AUlHcP6Kwb6Lj.baODxEJ2-qjG.8Baq7.9TF}
pwn.college{T7AO1dk8F.pD7YjeSGFpBAjGxiQqMERG89p8DJ2SBc2SRh6}
pwn.college{trZ1rcx.opIyqgErtTkkRYqC8i2SfzCX0EyJDarKkq1OlA0}
pwn.college{z2UbcD.lIHwrgEjFmXkH.CuMDMUFsgBaP5VoapKGq6oBWaB}
pwn.college{-LxtIxJsDhZScDUK-fJ1e9xEvXPqFsUCipYhztPfpc0Z0nY}
pwn.college{fC3Ng6ZTXlMrZdUPBhvCsWKVWOqYLRbmsIXjw7WuHrg4UJE}
pwn.college{NNlvpOQsMVjhW-QtfdnCsYPVyXVS9BvudV6wVKWoric2u9K}
pwn.college{5Q.a-qAZGzhVTaNYIOhvy7wKQEU04z5OotME9cq5p6Jxbuo}
pwn.college{jz.5ay8b1ecTeVOwEli6wyKZOwUN8EjpurCM7ZxyctrSvfM}
pwn.college{dADx8Ozibyd.s0odDRAUYX3BHizop.FJXinjttiwHGDi-ub}
pwn.college{lSX5RYbpMvyq9DCr1oZfzh4eXfvWz8kee1asS.e21QiijDi}
pwn.college{GIPrygcE7zO0Wx9W3dhMHyV46DutS3xaYxp5r8LNskAo0Ma}
pwn.college{zyPxPA6t6YpnXD7FiuQcrHqgpXbRpmg6ZhBfHp-BhDN8H.g}
pwn.college{0msAKnnuUdE.drU6Lk4hrCI4.ad3VYgCEGeSgdRVDUl0LuS}
pwn.college{KbE18FxBeQCnsYcvH0bTjISCFToOPfZbqWpFnpXYGVCi365}
pwn.college{ySYNgDnGtaMgJItwJGwjaC7DX38J3pBT4VqyQj79V53XSbW}
pwn.college{ZycXFx3T6f2Nr9xksdVu.pifVddTPHZuWC1J1m48bqy60DV}
pwn.college{a9TsO5LsJSH6BvXgF6VCNkItwBLduq2qhSSW3cQbwVhv1Ub}
pwn.college{C5iLOcwAssjUZ.inxUyOzeDYyGDzk5.XHbTyb9ZIbBuvUWG}
pwn.college{dMLu0IoeUYK...AwxW1cZf-Fdj15STYFMlEfjpiPz5O4qzV}
pwn.college{941Yf-.pb.PCmLlLofD59w6Syx4TnFLDprJl3HTGTyUq0Uj}
pwn.college{OzAQixEhNASeWZZuA4Y5ZrN-zvOpbjedmQTLNalbF6NVhZ9}
pwn.college{L8MtFBgQqmfjozQlSeVAlb92EWej.DtJfDNxCd2rLlRpm5g}
pwn.college{vSyIDieUgEsb3MusNu0CEod8LiWZRnCHWD3jKm1qNgvplcd}
pwn.college{55dauJ20e0.U-KEzOW0xpTMU6iaLpEedZN7IWOlZs-AaFDx}
pwn.college{z1.4bu-ug0czJJ5K6iw7J.hFdL3I5y5MBvHuXJKn57Z7tzr}
pwn.college{safVZZEM7TjqPAT48JuPxpspfvCJFAtsPkzDsqJdK0Ig370}
pwn.college{H3hsPm-BV0ODOCZabYcluw9nMWGwt0EC8dxk1SmIF3lApbA}
pwn.college{dmnUqAncQn9xAIY7e.vrk8KItslNu-NW3QpkWV5VGR6ULEF}
pwn.college{D50M7olP6p4.pdKB6ZsMp0hu6FLfwbqvjX5AVP5QEAPa0ea}
pwn.college{Yb1HJ1rIl.gim6zvkiFhfah9x5vkMIKg7gTh.U.I-x.fCKL}
pwn.college{9T0sD2xMVF7xD2XguYtV5vITLKu2Wat4r0l8GSCLMh4MIVX}
pwn.college{dlAg8AijZ4.tX4N3vnKsy37cUwInq5ntpoJWbt7KB7sCP2m}
pwn.college{t3mDQiQsLpTh3ERRIYSNQCc6oYGo0-jKxmN4Wt9L8LKdyYU}
pwn.college{YtVG3in24.NE1QQA87pui2TIm9V7xafxZRhcGq7mltvmwvm}
pwn.college{Q4jOuriaf4633F.iSnaV8I84HZZFFQq.aV77lqyrimZun7Q}
pwn.college{CSSxCmCIYE8.bBUxTwBCYFTt2WuOqRsp8nbZqTedOfXmJZg}
pwn.college{RlzK-clOZjcO.UAqrJRMdG.uphGN09ZPSIuFQw7smpMQfbu}
pwn.college{pqAYP0IRAzAufsXlSja6qsu93HxohyG2hrim9qr-FBCQPXx}
pwn.college{ZX5Au1mSeMcjfDqxBJnSYIh.djid.1GZphXo-Yr05lXNOqU}
pwn.college{Sbqx4eu7z-qtR66xtItVaK6jaVKqx2r5xFqaJoUyhJ3vbZn}
pwn.college{UwrRwO89g72o3Gh9fzsfCca89En4dlJ4BEhMZKRMKlsC6MZ}
pwn.college{H8C0wmYgbWaDXWLXl7k3gvqswbhjyvwL2L054x4DG6ngpao}
pwn.college{p6jbhI1Hmrne3iAcbg8rOX7Gw4beeFgYtE9mvgnDiPKoz6j}
pwn.college{FFLbU-BnJCirEH9UNqvDU9EPdXHDPwbtOsGluoDJef0IKy8}
pwn.college{KgW6LQwAnkcNclCqnRCO-s7xJHZmlr8mqrlVWhhCYUXizIF}
pwn.college{AGs9dzDsq.VyStBMjz42qcHkgn5Kd.sl.NRxBLJPKs42X7N}
pwn.college{LN-rN-KG-NIxCWZQuPJsEzhJW3iKgPC8Gioq8nQhgtX7dGp}
pwn.college{TfyEwnZ6893ghjxTkZ9OlUkRG1rr9Eo9ATsREbZ9P12tpwC}
pwn.college{bP3vg6nGShve2Ao-yjf1h4Kxra6kxiF2rB0y75q80bNsgC8}
pwn.college{DrMD6SbxGqZzMfzUgtrAVJPpifzmj7ICfB8YfXjpcQ0wnfz}
pwn.college{339MczhPE0Uv-5.QZitNwrvM2Y89GSg19WNn4.cLZrwugKD}
pwn.college{Hy16Rm3BoPeQy0rquxGj0Dsb2akmqfRgLIiCFHO3G7Stb0Z}
pwn.college{cnX3-nuAazAnsSdn77fCB1nnDM0u773G5shfmHpzODn2wxs}
pwn.college{HaL-TFdZNd4FFoOBbeyQNcHV4-n1nFYWmA0g.AO6W8ikueY}
pwn.college{TB0uZlBBAp5RmjlYzK79Wt3ccKfVdkDBuWxOlMMxxP9RHga}
pwn.college{09Ygvz1qzgnRr.PB5JSlOmZUO.g3wzrPYUZDtFKhBwjrakn}
pwn.college{rD4NldJxKFBD-W8dl-aWmCVJzmR.CeLlxGoe3vFULhrUGWe}
pwn.college{Ez9CRYkJiYJV9Yvtflx9swwp0HpJm0.1cz0J6TyQGWhBnwN}
pwn.college{q0Msf6BqEMroEvZVpf2qrvXlUu5whfV3ZJ4fSSjSSe9R77d}
pwn.college{GLzik.Af4hlzrsTaaiaDvzx-9HPedqGt7eNGVIIfss6mtHR}
pwn.college{14iMCFc-T2uqfUSN8o8XzTZ1gVJOPlM6XShIwTyUyO17Th4}
pwn.college{5IkhN5yb4.TT.dc8UT62cuLzIoOSUMoVOcyOOLXXnkH.K-u}
pwn.college{TJFL-6lKEzaX71h90HmIzQgSfh9qS3INVFIJr8mSDFf8B1v}
pwn.college{UjMpsuWiw0mSc61iCSvZTgG2T9Lh2Xha51SVkJp2Y1vxle7}
pwn.college{pGXxQo7gJnl1m5AB2PoCUvUP3bgwjefQCGV3bZhEfMnVQHm}
pwn.college{N879bRr26bc6b87kEAv3En6S.a25AzGW9aiLYZC5wTFHe2s}
pwn.college{3ClAjrqPawReAmg2NBlgPIc083ZB3QD.D.QSPAsCo5QSbqx}
pwn.college{wJcSMQpIbdTpUSRQkvo-Pv-mPdpzBDu7eeEooDAjP5NsPnG}
pwn.college{zst0GTspgnmOJldKLFv2Iom9zuv.AISAE8BYTFjSrJAJvXy}
pwn.college{ts50OzViks3kDrvNGJFjvCL4XydJM4DIHE49r0xsQuKmgym}
pwn.college{-A5kKxlJ-Or6z4p2Gtwe.rdVmiww5lWHj6rdQVMoNH1MZ9n}
pwn.college{HRyCoJZKGHKESY9OInX46pId5W6XC0ZfvLX6Tdgt4OdMbGh}
pwn.college{tZCPPtGXZrCYl0wSa7hVZ0RIjC-f-dTCEitzAVKDjzsMtf4}
pwn.college{8dfnUHmxaFwiDaOpViEwMaWZ.IEba.NnxZrFu.a0yw0egyU}
pwn.college{ggbZOSg5ZPXqNG5Hy9tKcWwORnMg3UZCbSd0aTofCN13J1x}
pwn.college{3GgRmFIDj6T.bOsrfhe4Ec8ria89H7n0qhy17U0-5aP5mxI}
pwn.college{tz8..MxZtnIws3tpxk7fvHpWPQE8tS0.UR-qAGA3RsvebwG}
pwn.college{88A3b.Dw3Wx43S6HASSwLAcsRvY30GmuOp4zmClBVAa8Mtr}
pwn.college{oqZidAoeZokDG0NpiTiEwT-KBdKFca7SOwG8t366DVgmvlj}
pwn.college{LGuQugT0mNCwxUlMT3-Dh8J3Ie-PH19na4TBRR3vgfM8t5W}
pwn.college{XuYXaXxINMeLpOnuiwA6H9y4LzC1qlBrIwO1Wn-sHC8CYF4}
pwn.college{.TpX4nQjxprFfNI.ooMOZOny5H2Sb.jec7Bru2I0yhz47fd}
pwn.college{f25Soo3sFHo.Ni1KLGN4Uw.h8iqY8saU9RfxHAZUcCYLNzZ}
pwn.college{FvR2NQ-2unt2aW6zc9Wg4N3vFy54ZjOY0SIvAdTDs0aMIIr}
pwn.college{5gwlAfZp3myDUTgSYP15EjGFuyeauO7MgUsvtbCmJpr2VRz}
pwn.college{37eDix4iPz0vQC3KzFriILLZFUYvhta36LIrWvMZB6XKUd6}
pwn.college{1I6MqdUFq.I4Y1kFZpcriupn2UYxV-nRZr6YV-rCLBneYq3}
pwn.college{EaYtH6.RGNBA9ucIf24Izc20d1Fb.LzB2uNgAf6fBa6Bbwh}
pwn.college{cInGcQemOkGSjHvTZKQ6vHPAq2FwJFiW-NqBRoK-IX2cM51}
pwn.college{b5dGnlWvw0oczsNAGkmLYE8l-mSjLmcJCV1cFFTCLAEjVms}
pwn.college{Gekdhce.QXTPeexerTxkl65wqVtMQywbWRW.lH-Vio.rbo6}
pwn.college{JAMKDuzgE1Cvz0A0IPCH-Hzb.xV3SD5H03OcpQsWxQvRSW0}
pwn.college{TsM5cnT2Q2pyieJ0hf9PpXCMVxjRcKoMEHd.A8.IV14fvQA}
pwn.college{BtIVGNDzSwOySNF3854anFcGGnjRzysH3sVt7FaTDdEeIf2}
pwn.college{vlhLGq1-imnXZmNEheDAPNKDqPWEZYLlRLo641D6x8kQbod}
pwn.college{H8hHoBm7lCEDaqz5pyrf0FkEJAKnhMjQ3zmJxKijsEU4BtI}
pwn.college{4nIKp4BLeeZX86DWPfyYZcE.6Q.3OxBsIhDgWG9u8nLzLKo}
pwn.college{nCBYa8KmiskLMt6IhHuhhzJpWSXWfnBKVuw-OVBDSsEPMAk}
pwn.college{IjQRTNlUk0GxZzDixDq4h9dyfpGUeBmzSMN1rYxqVdhejTE}
pwn.college{0XxAefCB48qKjFIaInYRM.xl1GiiOEKn.kTfqojuhHTMnvG}
pwn.college{xK1xZH-zoVcWcc1XY4JksEXZ3E3xIdNnak-6dbElH6z7MDX}
pwn.college{LJSgE7OHKsY.ro-nceOWM4ZOI8J3s2YLfB-Kz4l5xhjmCaH}
pwn.college{YSW.KKjAzjgPoeV7.YlK3QYLHKXRUoSmZlEYvTXukCWH9wH}
pwn.college{4V6pp6zn8WqC9XRPN9IHGTOJ1kN.jVKWpye4V-SeEwtclks}
pwn.college{kLiZJO7Oe.imL8LmsmZ91xb6JEDBBf4yW33.zlad0BrhEJf}
pwn.college{lGXXoWyV8okqnpwQAEPjsBUJiBqDIArGk.Nhvp6d25.bUky}
pwn.college{0LR34lDwQxhSwbvdHBIsLazsy2.sP4J5ONeNyAEYbnMk7Iw}
pwn.college{hl2Si4h40ffpw6PoX-yS4fDxF83eRZqLqgRiAdWpCOwtmjR}
pwn.college{Rbv5Y0fySX8lOutyIJOQxsBmu0O1z.QG-TiueQuueEBuVho}
pwn.college{ZIZ5ncCChkEQiw8CCgEgLGwJ0cfnn9gX00SVh.xzgxUAtyj}
pwn.college{.Ay0zAXwJhjn-0dP1-2yRTQeC8uX41TnwzMDoFLJsIe4ZU8}
pwn.college{cWe1L7duJn98XvEGVvMm0ZRNEpex4CJmgZH-3Pxvy.YUoCq}
pwn.college{3DxkTaudixhNsZLyDLcOwfqvjZLCpphPR.7zNK9.mq5D14T}
pwn.college{J1Yp.ywGh1nVrfW-eXwz67qqGeBQxsOk3o3yVV8y3g.1IQY}
pwn.college{SHpJ1llLTjH05.G6OWLSehsQ8zrXbPBnlU4GaM8QP.Gp5mT}
pwn.college{U1.y9PySyId6uH1S0E2ZsqzzckCSQ9a2dNKYWOGzzaocClA}
pwn.college{g7DMt3hh3C2eSQckdVdzTTBAf9cJVb-7WhzEI3lnzx.eHym}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{AKk2aG8Z4iS4zv67UWhmvpVxf8H.0FNzMDOxwiM1kjNzEzW}

```

## What I learned

Nothing new to learnt as this was just the practice of all commands from previous challenges combined into one. 

## References 
None.
