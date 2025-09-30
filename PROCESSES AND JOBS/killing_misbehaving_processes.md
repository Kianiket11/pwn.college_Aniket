# Killing misbehaving processes


## My solve
**Flag:** `pwn.college{AKk2aG8Z4iS4zv67UWhmvpVxf8H.0FNzMDOxwiM1kjNzEzW}`


```
hacker@processes~killing-misbehaving-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   17:58   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7  0.0  0.0 231708  2560 ?        S    17:58   0:00 /run/dojo/bin/sleep 6h
root         137  0.0  0.0   4132  1280 ?        S    17:58   0:00 /bin/bash /challenge/.init
root         138  0.0  0.0   4132  1280 ?        S    17:58   0:00 /bin/bash /challenge/.init
root         140  0.0  0.0   2744  1600 ?        S    17:58   0:00 sleep 6h
root         141  0.0  0.0   2744  1280 ?        S    17:58   0:00 sleep 6h
hacker       144  0.0  0.0 231576  3520 pts/0    Ss   17:58   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-
hacker       150  0.0  0.0 231972  4160 pts/0    S    17:58   0:00 /run/dojo/bin/bash --login
hacker       173  0.0  0.0 233600  3840 pts/0    R+   18:03   0:00 ps aux
hacker@processes~killing-misbehaving-processes:~$ cat /challenge/run
#!/opt/pwn.college/bash

fold -s <<< "Sending the flag to /tmp/flag_fifo!"
cat /flag > /tmp/flag_fifo
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{fPrCygg.aR.Ca3etF94RlK3LweYUAwAFHyX49zSyJTeZRhF}
pwn.college{68NUzcMRMRx4uMgVh7SphFw.GQVVh6TfJTQe8dDvV6lgLCC}
pwn.college{a0qCTMRM1YBswDnUtXPSkfM6tP0qo6HXf0QwEVyC99gNCx2}
pwn.college{yG.cmmKHf3GXgY1f-hk5BAfYP2-J4nJ98hNF-lTFXrE8ltI}
pwn.college{1iOvY2MTzIfvEHJYFl88VjS9Ye2zM9jbcK8ODcLcG2XqRfA}
pwn.college{ve43yZnvLkp2Bxgm6MZwmU0PrCi0-TjsxYif1qP5rqJeJf9}
pwn.college{DNhw0h1e4ilK5y5TBdo4gAzLdGY4-LYmnAzDDHZTqwdmCHM}
pwn.college{LXCI3qyne99t.QCP-69YmHospoiclo2c2kh0O1WR4oNCsZ3}
pwn.college{8WT2R5AkJi51BkPv9WGiSE8FAmJTucMaR8eflBTIsFoGZjm}
pwn.college{G.S5-4DEkMI5L6DwDjYkbMPZ2mw3pw0PWHs9Vv0df57z14j}
pwn.college{QES1mgmor5iQ1pDeaAMA68lx2d3.Hibl8PIMTnwCPJeEx-5}
pwn.college{18L1Rb8-aGzle2Yd.wK3zKj6SKGhCUk9s6amLBaXdM8xzYD}
pwn.college{zw0e4Q6Mn2T8xTi65c2BIpVZS9ZBcha1RN44pyxhL1zBuRR}
pwn.college{q0XQ9AHvMWFyetPOgCAfQDBfBDlW-tGw5QNOmYy3i7.hGrC}
pwn.college{VQ9mzs0Ay80dwIghIZftcz8b6pha6LTZkKC9snwk4-jj35b}
pwn.college{tOcCaj9Cji9y4Pl9Awcrc5StHSBkrOT7nGd0-y0ezLv4TC0}
pwn.college{EB.4YEgVDr7eQI.JaG7Z2jaFXRjE3hqsOfKqxM0GSuYoyTO}
pwn.college{pOuhHgjqf-iZTmqDSCKA-NFk0P6dFQXRnYMfhSlK50nDBfJ}
pwn.college{yPdGG-WkFq0MpSizmJGZRjpljsZFEyg5ZE8nlT391Sb26xM}
pwn.college{-2TN8oOuv5aD4mSfH80hfBX0VdPWEDpzSOaGpOuCRyoaPoY}
pwn.college{sh.pIaymfwv2nymmUoIufUcwUMDjburCNOEqfpnj17UQzZR}
pwn.college{h8HU6sEbmU5h2WaOylstIOBSU8YA47qU8YF3C7BPtuCmjAO}
pwn.college{GHw.8DGaJfvvJ-xIm6XjUo9EsswilJmDdmgNek0mTRck0ix}
pwn.college{HTH6m8ntx94Uu-age6iNaZyDs8rzF.f2XtBspLCDQ4DgDOe}
pwn.college{8tdmal46unT6XM3JMYNFBC7vI42DrdnxiCwbvfxIBmLE.ao}
pwn.college{BFyD.1jF1RLGC6V1sDuCvBSzn9PIhNlBjsRoulbUqPxleUU}
pwn.college{sTzQe4p3vDCX4EnD7XJgWEKEiTK-IiCivMeBbhlonyTglda}
pwn.college{gQEhmqwTH29KWnjOgNKKRjDiiQ87QLDBE7m0tb9DgPtytRr}
pwn.college{lBDGr4qONRTYLByqZRZlxOu.VKdx8ZL1Jp7MhyrQHH6iW4E}
pwn.college{w6ZBIIVJnrHAijt4x1wiyk7EsN8jA5JvQHydqptXu5XQM1P}
pwn.college{SbhwG.lQTFXsWahbHZ-Dxj57vyvk-v3YZPuhh-L9rk96bSC}
pwn.college{w9zHtZq0tHI8Rr1.-.gQ5XqQGZiQX2BqVWkCm5UhPLD85WD}
pwn.college{wiHZ9lkPm12ZwDRA6i.uQnabiBvSvCfZ1rWQCXBwQDWnRFO}
pwn.college{oLYkR.1K5FsxgXM6NYuUglWo0KSuhKqRogTnuxaJnD5rxZJ}
pwn.college{fxRNpjn0DH9wZjYFWK3LNrWm6vlC1RN7rzqRBfoFZpPzuPm}
pwn.college{YD9hcgJRalgmPAfo.o8Gy2DtqEBs-pW.eIwAzX7md-iACue}
pwn.college{Sn1OgAC4TXxLyQOw6gksLZxAP3MmNZIi6UT-mv.OKbdXlkU}
pwn.college{jkTIT8u1BxHspWUkefXVb4AkqtQHBuRo31VXbpD01L71UqJ}
pwn.college{4njiQhzVTpjvFhUh7mndJHiBqdFbpT3uN0pgIQ5Cp11ZG3D}
pwn.college{ACtMMyYo0gjObfy1RlGmpmTp3Z6mGj9t.eXmbw84RfIXaDx}
pwn.college{SnO0rBkTxsGkP99Bv.nizBBoS7dj07Kv897u9iDpeadJLCv}
pwn.college{8VB2FIktZ5ollgRvX.Nj5Rv4hozObP0tYLDlX1UkeaLla.c}
pwn.college{iEUSn73W.StMb.MbwmDMlq8V2fdhyKy.D3FRvEvqA64UWGo}
pwn.college{eI74I1mnQ2J.xUBjIzBOpWo--uhyowbEnGcbiDtI6ll8BMS}
pwn.college{evjaGVIv4CX5gRaXRHRobysNBkavZR7xXfJfE93Fmo5-HJ1}
pwn.college{SFQQZZpWYL7NrZEtHZ4O.xiTYkyQhQR0-kiKLJiYk0oxoy7}
pwn.college{krgmu7XOW31G8-DHsGsa3L7YuMpTi2hC-z42gQelwdfN70l}
pwn.college{lDkmWfOUYcN1wkAe-PB6JEybO14J4iDsPEWSDXuNgT5W4ZB}
pwn.college{rVe8-cvWscZHgSGHf9ZW-fpj-jM7amqXcFPV.cgtuxcgn3g}
pwn.college{RmMGrlvO7QbcaKw6i7bXfTT.PfWijVwOjlZGskM5oEHHx4u}
pwn.college{8jhkn7Q4NvRLFiy0RLHjN95VToEGtsfMPW4jy1tX07yEktD}
pwn.college{GTMWG3QEKMFLwmInZhGqxJunlZl9gCk3YOLtHbvcSoyhE0s}
pwn.college{JZXrn1yCqm6s9zjbeeEcEmRnI8xJdzNAgLK2OQRHd6Z4TWk}
pwn.college{eYSunuc.THAuvtHK-mFlPYXArIn9hAn5V1VSSacPB6TK2qL}
pwn.college{Ir0ga3UxE.vUQi-AJDrbHZndM5jcbcp7SzgA7JW-9OLy3DY}
pwn.college{3MNgXLMiSYr9lwrf70toXcGlszbTxDdX78T-Lk3-5bOUXAG}
pwn.college{bNP2138yggRfkdxHDu-5Kt1dj-1OM2pqmvhqvvrMddKEXik}
pwn.college{nwxZ520PwZv-nxyt5toyEuynLgCUdeXCOLNgnS3Smg9m74u}
pwn.college{LobH8KuqciMXG.Rvvow7ZZJTDgmXUPzN.Xgp90T0xnWE.pL}
pwn.college{ZS1bqf4iWXW6WKQP97peB6f-xGKnvNArxuSsaz8COQ8qeMA}
pwn.college{3LOMcpi3kKuk6pWws2iiHovw.orRd16YcIvMndpEcdNEkUF}
pwn.college{ldhP4TFZC6GD-12pJdn9GVTbUMRkzR5s8SzJXUv9-Az6doG}
pwn.college{T52mXPgu-jycTBSdql9fiGEODPOZ17SXlNFykm9oAAWQzWL}
pwn.college{EmhVBy7drVkVJf3rE-MW36RRMpiM.NoGXx5vDtQ9JPseN.O}
pwn.college{1NbtNEOjBWcFnvm7PRYNm4n6zK7.cKAITDkT-yeeyi3v29.}
pwn.college{pGr0iom5It9aMXHwj5thnAf4wH3ACBmPELTYFi3PtyopJ7A}
pwn.college{2KvpmsJ94SKt0TX5QnSaIFco9LBSWONM940MDsQrZBET.e-}
pwn.college{.NW3puvd2v862-BIzXU8jQlE5FaTI3CRuRKi6VJJ6Vsb6ru}
pwn.college{z6PxzcLLB7vEzJycR83WWa0eCKZYzobZIoC0I9Pn2tbLwYg}
pwn.college{EyIiS.jfr9WBRkkJzotkuMv2P75CGLGG2N6ByLjuqTX0kJL}
pwn.college{OlseM4LhBeDC5guORNP9s0zThHh9296gQ3iviFTOF91kMcp}
pwn.college{04lIw1DOV88m8C.zJviwGmbJ5VtpAj6R7HJIVVk2udoklhW}
pwn.college{X4.shMfR-5o2o0Ay76BL89becOirNDg5z2IjZcrGnD0AFa8}
pwn.college{4llNmvf8du6nQJ0YZuQB.ZvaMlb2Uq2vFMbBFYwQ2bl2g54}
pwn.college{999gnGHztQ2G7PDSL3feXnnjZU3inFbLOPXKqcmndzdVt3W}
pwn.college{2Q2VF1iHRTYGxkeaU9uN4UGQXlg4KgcA2-cvpVWEf0NybbB}
pwn.college{2a07t7LKJj3xPZEzLd3B.ASDYi.FVhpdDoFFgcKJf1.Lyhv}
pwn.college{Z9lJrX7sSCb0h1f.N-HV-XXPUSqsVEnHNFWAKPkgjIVq.pB}
pwn.college{DRz0BY.I6mSxUqP3hycavdjzvuKXpGUPv9jb0tMLiGAsc7q}
pwn.college{dPltiDCsyPNiNyCHGDxOVikzcvXPtx8CwiROhPcfaN-Kdf0}
pwn.college{lfjlVkkGPUfDNa5Ec65jBXQquNkHIcSpiNZEd.Qqnv2GnvK}
pwn.college{3v.G6lW-OgwsqUUvCjrYwx08fU5P.0ittIPPqjmGIonR5fc}
pwn.college{cajHDWoeChllcrqfx8nQC9sf996qvzEN5ruWTU5dr75vQuA}
pwn.college{0ZznmTHX0UiAgGlpraFWHzIGdicem6WzpBQj1xB-ZDf7qdP}
pwn.college{mgr0Dxe9xAXYUn-whxOXejH66bTkxOTJoVy-SAcbPEvNDXl}
pwn.college{JW282i4lxDopZf6AQSzeC49mSxL3CjNUMU7wFt32tcMDCpP}
pwn.college{WfqqjKVK1Gc6FwK.cHD.mBPXgS5SmjD8Q2CqG17W75aKPYz}
pwn.college{gf.y5QfrjhyWBZROz.ZRqD0CZZ44LohUTm9CAQ0L2m0kC.0}
pwn.college{7GJVy437jVt1TdapunDq1LR25ZljTQDvQnehDXqdOu94D2I}
pwn.college{OooRroY-HZaIAdIvQwM19MdkgvEXb7pSFVtpKeOSQnlr6Ul}
pwn.college{VnYRFilh0j0VsqvnpsemFSIPGvts4MF7Frxe9YOAQLKqBJV}
pwn.college{tQEDlkb6xNBHoxLzF47RypPN.oDs6MIgk6pctoRdkaHWjl1}
pwn.college{52M0Z4GWsF5JofRrXis.n-SU7fuhqqvO5I8fYtF1372Oku4}
pwn.college{paoXZOozZLnYpVdaMsXwPeaSku--hYhbmxqyUb4cu5D.eaJ}
pwn.college{AYcS.kRaT7KER0ya.UAXNcMuJMcqwgl.pQPXlK7v63PAR9W}
pwn.college{kgUZpBZkk8zhTglIDYjK6.FI9zIqktCNk0uM6InGGP.RaOh}
pwn.college{5HB3UpzZYxr1r.13dqCL9JKa11RuYWZU5GxF.z6F0y3rZ.q}
pwn.college{2OZW1PNF260aOMzuzwqDFHwu9EJaKYopuZumiL.TYcePdJ1}
pwn.college{sjSpEXSQJUroS2t1DiwvsFG8yb5CPBzCChp9IUW5nUE8AKi}
pwn.college{KD2y8h5wOERvPACRtsMee5niTGvaaWW-QdUGbn6UWOvb41u}
pwn.college{qhrruRpYEDCuLhj8VtceRSjPLwmpStljDHvEF.QEgjSBznE}
pwn.college{UtLNkqgCONY3O6VgK7HKtR8608-uCMrEekpnNwE9J977W1e}
pwn.college{oWLTwll9z.hp30MQqAnJJpvI0PmO9qh8nyRCSv1o6o23hL2}
pwn.college{OoaPDwTFyaLCiScJ1Yi5llB4wy2DXocRT31lh8k32crXySs}
pwn.college{InJULZWwQkV6To8YgKf-T0MBjPW0ffun1BZibNrN.mwnVXf}
pwn.college{F6j8wwunRIS0Ck1AIila8a9VI2zQ2X7YcxoLPAmjMaqEw17}
pwn.college{rGzaFPtx8PnRNs7g7tBvQ0FajXuPcQNfFyHUCHE8.MGCdMT}
pwn.college{DB.8k3n6axKYhqdXt13GLhqX-5S6wjm8aMpOesZgnowSSjn}
pwn.college{RoCzU4AHLdq8jwp-49tVPovZE2CRt9m-7MmgVolm7jCLl3P}
pwn.college{rD9Tb.L8CAMh5rWZXhSumfw4BxL97DYZUmMaRqtZGUt-c3U}
pwn.college{Fa-FG0MElbMbZ3rBROgWimQLL-fB2WysBx3yYUFosW44HgE}
pwn.college{6LmwQcdSwiCorl7wyLqwoF20tUPvAdVsA17ibTWEbnWNmox}
pwn.college{z.V7gRDWvzvLiBkqPHYFbJWkH7NwM-VCRyzd9Qhcz64SwxE}
pwn.college{AvaLHqttdZtIY5K7YL.N0fNQ1L1T9iYkVJY8cuk0cdbGmgD}
pwn.college{7XoRIO6embl1HuSSn4jpBFke2RQhkb.W2vHoj.vZAoGgucw}
pwn.college{gQQZk1OsSMnt8wG8gnDqLzXSnf8.9v0plnOEVpHjUDMyMz1}
pwn.college{nYjq9J-Be2sNohOcx7Sn0iGC0Fg4fII5rgTTCVLsQFbpcXV}
pwn.college{WWevjOVv19kmS0W8HFfv1d4HQGi-EMekhRfuYpoLlyAhlyl}
pwn.college{9.cE96MU7ROYnrbNZxFcSUUNT7kZbBV3BspGsI8s0GhImCj}
pwn.college{FdfH0sdDyWCsV98-dbBMva6PrhyFLpcwPoIGvX5xBRqf7S0}
pwn.college{vvmO7hqZ3yX01A.jtJO7smDt0GPFMZE1eFQPr.b7CoJrbFR}
pwn.college{LYYGAFv.V8dhhapfHujqoDoaFB-9yfUGyYbO-WUg1MlLrUB}
pwn.college{6Vcy0dsy4TUaN7.PYeSMa4yXJDNbiiLJIWenNCKyMQCzGvp}
pwn.college{TyTwa5UsyxGnpexg6lN79d9uPqz3nxpmiho0mCbgY.mbpFB}
pwn.college{j4a1m71E2Dw5qb8ElBtpE071qmO8V8J0it893iGgIa8UzMh}
pwn.college{SnqJhQ0ZHdgIeIJzpKayJMvc6Jaro0WHHApB1boPURfM5FU}
pwn.college{PzwkDQBBXilh5W4qnqOtIj3MjCy8RMUPFYh.vm-YQ0vuzpo}
pwn.college{UoQl4ZsDyRttunf3gWpG7ZSTztjHvDwzPCypAu8dKRz09wm}
pwn.college{Cef8zi2jIb9.YuBuQkzniaCF618-X5SBIdvFwa3iToO29Ng}
pwn.college{IRTaLyOHsK4423DtW61yjCBijjSv8Qfb4i2BD-pyZUC0fVm}
pwn.college{eg.8J1M72wfQB8FLGxbUfotHtCwbSkj2-KjgqCRw78L9wok}
pwn.college{v8q5xFXrsgb4HRfwbvh2aCB66ZXddxXCtxOZ0cfjxWQQKT4}
pwn.college{LUNJJVoaTv-s0Uxlls7V7oO9jwYuwX-L8iiVD5DDbbSy7TC}
pwn.college{gCXs.MwRLlLdSA-Kt4YLBLaBwmhZYEOzdy3u5ur6V4ec-um}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{AKk2aG8Z4iS4zv67UWhmvpVxf8H.0FNzMDOxwiM1kjNzEzW}
```

## What I learned


## References 
None.
