# Extracting specific sections of text

In this challenge the /challenge/run program will give us a bunch of lines with random numbers and single characters as columns. 
We have to cut them in order to extract the flag characters, then pipe them to join them together into a single line.

## My solve
**Flag:** `pwn.college{4op_5EMG8M2-Rok7vPgy1oTEA0c.01NxEzNxwiM1kjNzEzW}`

As given in the challlenge /challenge/run gave us a bunch of lines and then we can use the cut cut -d " " -f (coloumn no.) to cut the 
coloumn we need. Now what i did was i took 31889 p as 5 coloumns and ran the command as i needed the fifth coloumn and i didn't work 
so i used it with 6 thinking i did counting mistake and tried to extract the 6th coloumn but it also didn't work. At last i used 
it with 2 as there are no spaces between 31889, therefore, they are a single coloumn and the flag is in the other. And finally, i used
tr -d "\n" to remove the new lines added like in the previous challenge.

```
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run
31889 p
10406 w
26764 n
19803 .
18803 c
7678 o
6525 l
5799 l
16195 e
20762 g
11756 e
7569 {
13235 4
21602 o
29530 p
12583 _
10894 5
27890 E
1014 M
4090 G
26157 8
15729 M
20734 2
30568 -
23892 R
30022 o
20911 k
26932 7
24237 v
17426 P
5807 g
21236 y
6001 1
4192 o
10809 T
2700 E
931 A
25696 0
5034 c
7227 .
5602 0
12290 1
27684 N
27025 x
19434 E
11210 z
25584 N
19451 x
23620 w
3650 i
8933 M
102 1
15142 k
30849 j
29072 N
13569 z
1629 E
19781 z
30072 W
8882 }
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d ' ' -f 5 | tr -d '\n'
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d ' ' -f 6 | tr -d '\n'
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d ' ' -f 2 | tr -d '\n'
pwn.college{4op_5EMG8M2-Rok7vPgy1oTEA0c.01NxEzNxwiM1kjNzEzW}

```

## What I learned

I learnt about the cut command and how it used to extract a specific coloumn form the data.

## References 
None.
