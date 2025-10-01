# Sorting data

In this challenge there's a file at /challenge/flags.txt containing 100 fake flags, with the real flag mixed among them. 
When sorted alphabetically, the real flag will be at the end.

## My solve
**Flag:** `pwn.college{c_cZipsLN8n5TuqjacFnJGw3qrT.0FM0MDOxwiM1kjNzEzW}`

As given in the challenge that /challenge/flags.txt and we need to sort this file in alphabetical order in order to get the flag. We can use the sort command and by
default it sorts data in alphabetical order and as given the flag will be at the bottom when the data is sorted alphabetical order. 

```
hacker@data~sorting-data:~$ sort /challenge/flags.txt
ovm.bokldfe{c_bZiprKN8n5TuqjabEnJGw2qqT.0EL0LCNxwhL1kjNzDyV}
ovn.bnlkege{b_bYipsLN8n4TuqiabFnJGw2pqT.0FM0MDOxviM1kjMzDzW}
ovn.bnllege{c_bZipsLN8n4TtqiacFnJFw3prS.0EM0MDOwwiM0kiNzDzW}
ovn.bollege{b_bZhpsLM8m4SuqjacFnJGw3qrT.0FM0MCOxwiM1kjNzEzW}
ovn.coklege{b_cYipsLN8m5TuqjacFnJGw3qrT.0FM0MCOwwiM1kiNzEyW}
owm.bokldge{b_cYhpsKN7n5TuqjabEnIGw2qrT.0FL0MDOxviM1jiNzDzV}
owm.cnlldgd{c_cYiorLN8n5SuqjabEmIGw3prT.0FM0MCNxwiM1kiNyEzW}
owm.colkefe{c_cZipsLN8n5SupjabFmJGv3prT.0FM0MDOxviM0kjMzDyW}
own.bnkldge{c_bZipsLN8m5SuqjacEnJGw2qqT.0FL0MCOwwiM1jjNzEzW}
own.bnklefe{c_bZiorLN7m5TtqiacFmJFw2qrT.0FL0MDOxwhM1kiMzDzW}
own.bnlldge{c_cZhosLM8n5TupjacFnJGw3qqT.0FL0MDOwwiM1kjNzEzW}
own.bollefd{c_cZiprLN8m5TtqjacEnIFw3qqT.0EL0LDOxwiL0kjNzDzW}
own.cnlkege{c_cZipsLM7n5TtpjabFnIGw3prS.0FM0LCOwwiL0kiNyEzV}
own.cnllege{b_bZhpsKN8m4TuqjabEnIFw3qrT.0FL0MDOxwiM1kiMyEzW}
own.cokkege{b_cYipsLM7m5TuqjabFnJGv3prS.0FM0MCOxwiL1kjMyEyW}
own.cokldge{b_bZhpsLN8n5TtqjacEnJGw3qrT.0FM0LDOxwiM1kjNzEzW}
own.cokldge{c_cZipsKN8n5TuqiacFmJGw3qrT.0FL0MCNxwhL0jjNzEzW}
own.colkdfd{c_cZipsLN7m4TtpjabFnJGw3pqS.0FM0MDNxwiM1kjNzEzW}
own.colkdge{c_bZipsKN8n5SuqiacFmJGw3qrT.0FM0MDOwvhL1kiNzEyV}
own.colkege{c_bYipsLN8n5StqjacFnIGw3qrT.0FM0LDOwwhM1jiNyEyW}
own.colkege{c_cYiprLN8n5TtpiacFnJGw2qqS.0FM0MCOxwiL0jjNzEyW}
own.collefd{b_cYiorLM8m5TuqjacFnIGw3qrT.0EM0MDOwwiL1kjNyEzW}
own.collefd{c_bZipsKN8m4TtpjacFnJFv3qrT.0FL0MCOwwiM1kiNzDzW}
own.college{b_bZipsLN7n5TtqjacFnIGw3qrT.0FM0MCOxwiM1jiNzEzW}
own.college{c_bZiprKN7n5TuqjacFmJGw3pqT.0FM0MDNxwhM1kjNyDzW}
own.college{c_cZipsLN8n5TuqjacFnJGw3qrT.0EM0MDOxwiM1jjNzEzW}
pvm.bokkegd{b_cZhosLM7n5StqiabEnIFw3pqT.0FM0MDOwwiL0jiMzEzW}
pvm.colkegd{c_cYiosLN8n4StpiacFnIGv3qrT.0FM0MCOwviL1kiNzEzW}
pvn.bollefe{c_cZiosKN8n5SuqjacFnJGw3qrS.0FM0MDOxwiM1kjNzEyV}
pvn.bollefe{c_cZipsLN8n4TuqjacFnJGv3qrT.0FM0LDOxwiM1kjNyEyW}
pvn.bollege{c_bZiprKN7m5TupiacEnIFw3qrT.0FM0MDNwvhM1kjMzEzV}
pvn.cnkldgd{c_cZiprKM8n4TupiacFmJFw2qrT.0FM0LCOxviL1kjNyEzV}
pvn.cnlldfe{c_bZiprLN8m5TtpjacFnIGv3qqT.0FL0MCOxviM1kjMyEzV}
pvn.colkdge{c_cZipsLN8n5TupjacFnIFw3prT.0EM0MCOxwhM1kjMzEzV}
pvn.colkege{c_cZipsLN8n5TuqjacFmJGw3qrT.0FM0MDOxwiM1jjNzEzW}
pvn.collefe{b_bZipsKN8n5TtqjabFnJGw3qrT.0FM0MDOxwhM0kjNzEzW}
pvn.collefe{c_cZiorLN8n5TupiabFnJGw3prT.0FL0MDOxwiL1kjNyDyV}
pvn.college{b_bZhpsKN8n5TuqjacFnJGw2qqS.0FM0MCOwwhL1jjNyDzW}
pvn.college{c_cZiprLN8m5TuqiacEmJGw3pqS.0FL0MDNxwiM1jiNzDzW}
pwm.bollefe{c_cZipsLN7n5TupiabFmJGv3qrS.0FL0LCNxwiL1kjNyEyV}
pwm.cnkldfd{c_cYipsKN7n4TtqjacFnJFw2prT.0EM0MCOxwiM1jjNyEzV}
pwm.cnlldgd{c_cZhpsLN7n5TuqjabEmJGw2qrT.0EL0MCOxviL0kjNzEzW}
pwm.coklefd{c_cZipsLN8n5TtqjacFnJGw2qqT.0FM0MDOxwiM1kjNzEzV}
pwm.coklege{b_cZiprLM7n4TtqjabEnJGw2qqT.0FM0MCOxwhL0kjMzEzW}
pwm.colkegd{c_cYiosLN8m5TuqjacEmIGv3qrT.0FL0MDOxviM1kiMyEyW}
pwm.collefd{b_bYipsKN7n5TtpiacFnJGw3qrT.0EM0MCOwwiM1kjMyEzW}
pwm.collefe{c_bZipsLN7n5TtqiacEnJGv3qrT.0FL0MCOxvhM1kjNzEyW}
pwm.collegd{c_cZipsLN8n5TuqjacFnJFw2qrT.0FM0LDNxviM1kiNyEzV}
pwm.college{c_bYhosKM8n4TupiacEnIGw3qqS.0EL0MDOxwiL1kjNyDyW}
pwm.college{c_cYhpsLN7n5TuqiacEmJGw3prT.0FL0MDOxwiM1kiNyEyW}
pwm.college{c_cZipsLN8n5TuqjacFnJGw3qrT.0FM0MDOxwiM1kjNzEzW}
pwn.bnlldge{c_cZhpsLM8m5TuqjacEnIGw2qrT.0FM0MCNwviM1jiNzEzV}
pwn.bokkdgd{c_cZipsLM8m5TuqjacEnJFv3prT.0FM0MDNxwiL1kjNyEyV}
pwn.bokkefe{c_cZhpsLN7n5TuqjabFmJGw3prT.0EM0LCOwwiM1jjNyEzV}
pwn.bokldge{c_cZiprLN8m4TuqjacFnJGw3qrT.0FL0MDOxwiM1kjNyEzW}
pwn.bolkege{c_cZhpsLN8n5TuqjacEnJGw2qrT.0FM0MDNxvhM1kjMzEzW}
pwn.bolkege{c_cZipsLN8n5TuqjacFmJGw3qrT.0FM0MDOxwiM1kjNzEzW}
pwn.bolldgd{c_cZipsLN8n5TuqjacFmIGw3qrT.0FM0MDOwwiM1jiNyEyW}
pwn.bolldge{c_cZiorLM8n5SuqjacEmJGw3qrT.0FM0MDNxwiM0jiMzEyV}
pwn.bollegd{b_cZipsLN7n5SuqjabFnJGw3qrT.0FM0MDOwwiM1kjNzEzW}
pwn.bollege{b_cYipsLN8n5StqjacEmIGv3prT.0FL0MCOwwiM1kjMzEzV}
pwn.bollege{b_cZiorLN8n5SupjacEnJGw3prS.0FM0MDOwwiM0kjNzEzV}
pwn.bollege{b_cZipsLN7n5TuqiacFnJGw3qrS.0FM0LDOwwiM1kjMzEyW}
pwn.bollege{c_bZhprKN8n4TupjacFmIGv3qqT.0FM0MDOxvhM1jiNzDzW}
pwn.bollege{c_cZhprLN8n5TtpjacFnJGw3qqT.0FM0LDNxwiL1kjNyDzV}
pwn.cnkkege{b_cZhosLN8m5TtqjacFnJFw2qqS.0FM0MDOxwiM1kjMzEzW}
pwn.cnkkege{c_bYiosKM8n4TuqiacFmJGv2qqT.0EM0MDNwwiM0kjNzDzW}
pwn.cnkldge{c_cZiprLN8n4TtqiacFnIGv3prT.0FM0LDOwwiM1jiNzDzW}
pwn.cnllegd{b_cYiorLM7n5TuqjacFnJFw2pqT.0FL0LDOxwiM0kjNzEzW}
pwn.cnllegd{c_cZiprKN8m5TtqjacFnJFw3qrT.0FM0MDOwwiL1kjNzEyW}
pwn.cnllege{c_cZipsLN8n5TtqjacFnJGw3qrT.0FM0MDOxwiM1kjNzEzW}
pwn.cokldgd{b_cZiosLN8n4TuqjabFmJGw3qrT.0EM0MDNwwiL1jjMyEyV}
pwn.cokldge{c_cZipsLN8n5TuqjacFnJGw3qrT.0FM0MDOxwiM1kjNzEzW}
pwn.coklege{c_cZipsLN8n5TuqjacFmJGv3qrT.0FL0MCNxwhM1kiNyEzW}
pwn.coklege{c_cZipsLN8n5TuqjacFnJGw3qrT.0FM0MDOxwiM1kjNzDzW}
pwn.colkdgd{b_cZipsLN8n5TuqjacFnJGw3qrT.0FM0MDOxwiM1kjNzEzW}
pwn.colkdge{c_cZipsLN8m5SuqjacFnJGw3qrT.0FM0LDOxwhL1kjNzEzV}
pwn.colkefe{c_cYipsLN8n5StqjabEnJGw2qrS.0FL0LCOwwiM0jjNzEzW}
pwn.colkefe{c_cZiprLN7m5TuqjacEmJFw2qrT.0FM0MCNxwiL1kjNzDyW}
pwn.colkegd{c_cYhpsLN8n5StqjacEnIGv3prT.0FM0MDOxwiM1kiNzEyW}
pwn.colkegd{c_cZiprKN8n5StqjacFmIGv2qrS.0EM0LDOxwhM0kjNyEzV}
pwn.colldge{c_cYipsLM8n5StpjabFnJFw3qrS.0FM0MCOxviL1kjNzDzW}
pwn.collefd{b_cZipsLN8m4TuqjacFnIGv3qrS.0FM0MDOxwiM1kiNzEzW}
pwn.collefe{c_cZipsLM8n5TuqjacFnJGw3qrT.0EM0MCOxwiM1kjNzEzW}
pwn.collefe{c_cZipsLN8n5TuqjacFnJGw3qrT.0FM0MDOxwiM1kjNzEzW}
pwn.collegd{c_cZipsLN7n5TuqjacEmJGw3qrT.0FM0MDOxwiM1kjMzEzW}
pwn.collegd{c_cZipsLN8n5TuqjacFnJGw3qrT.0FM0LDOxwiM1kjNzEzW}
pwn.college{c_cZhpsLN8n5TuqjacFnJGw3qrS.0FM0MDOxwiM1kjMyEzW}
pwn.college{c_cZiprLN7m5TtqjacFnJGw2qrT.0FM0MDOxviM1kjNzEzW}
pwn.college{c_cZipsKN8n5TupjacFnJFw3qrT.0EM0MDOxwiM1jjMzEzV}
pwn.college{c_cZipsLM8n5TuqjacFnJGw2qrT.0FM0MDOxwiM1jjNzDzW}
pwn.college{c_cZipsLM8n5TuqjacFnJGw3qrT.0FM0MCOxwiM1kjNzEzW}
pwn.college{c_cZipsLN8n5TuqjabEnJGw3qrT.0FM0MDOwwiM1kjNzEzW}
pwn.college{c_cZipsLN8n5TuqjacEnJGw3qrT.0FM0MDOxwiM1kjNzEzW}
pwn.college{c_cZipsLN8n5TuqjacFnJGv3qrT.0FM0MDOxwiM1kjNzEzV}
pwn.college{c_cZipsLN8n5TuqjacFnJGw2qrT.0FM0MDOxwiM1kjNzEzW}
pwn.college{c_cZipsLN8n5TuqjacFnJGw3qrT.0EM0MDOxwiM1kjNyEzW}
pwn.college{c_cZipsLN8n5TuqjacFnJGw3qrT.0EM0MDOxwiM1kjNzEzW}
pwn.college{c_cZipsLN8n5TuqjacFnJGw3qrT.0FM0MDOxviM1kjNzEzW}
pwn.college{c_cZipsLN8n5TuqjacFnJGw3qrT.0FM0MDOxwiM1jjNzEzW}
pwn.college{c_cZipsLN8n5TuqjacFnJGw3qrT.0FM0MDOxwiM1kjNzEzW}
```

## What I learned

I learnt about the sort command and how we can use it to sort data as per out needs as we can use the following arguments to sort data in 
our way :
-r: reverse order (Z to A)
-n: numeric sort (for numbers)
-u: unique lines only (remove duplicates)
-R: random order!

## References 
None.
