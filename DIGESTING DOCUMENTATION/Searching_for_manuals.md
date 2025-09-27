# Search for manuals
In this challenge the manpage for the challenge is hidden by randomizing its name.we have to use the hints to find the flag. 
HINT 1: man man teaches you advanced usage of the man command itself, and you must use this knowledge to figure out how to search for the hidden manpage that will tell you how to use /challenge/challenge.
HINT 2: though the manpage is randomly named, you still actually use /challenge/challenge to get the flag!

## My solve
**Flag:** `pwn.college{ElTLIiNV440vbywbC4v4tmu77Kj.QX2EDO0wiM1kjNzEzW}`

As the challenge suggests that we have to use the hints to reach the flag. So using the first hint i went inside the man manuals using man man
there i found the argument -k which is used to Search the short manual page descriptions for keywords and display any matches. Now i just did 
man - k challenge which gave me the changed name of the manpage of challenge.when i went into the manpage of challenge there under the description
section i found --livbyw NUM (print the flag if NUM is 440). Finally, i wrote /challenge/challenge  --livbyw 440 to get the flag.

```
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$   -k, --apropos
              Approximately  equivalent  to apropos.  Search the short manual page descriptions for keywords and display any matches.  See apropos(1) for de‐
              tails.
bash: -k,: command not found
bash: syntax error near unexpected token `('
bash: tails.: command not found
hacker@man~searching-for-manuals:~$ man -k challenge
livbywbvtm (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man livbywbvtm
hacker@man~searching-for-manuals:~$ /challenge/challenge  --livbyw NUM
              print the flag if NUM is 440
Incorrect usage! Please read the hidden challenge man page!
Error: no such file "the"
Error: no such file "flag"
Error: no such file "if"
Error: no such file "NUM"
Error: no such file "is"
Error: no such file "440"
hacker@man~searching-for-manuals:~$ /challenge/challenge  --livbyw 440
Correct usage! Your flag: pwn.college{ElTLIiNV440vbywbC4v4tmu77Kj.QX2EDO0wiM1kjNzEzW}
```

## What I learned
I learnt that man command also has a man page for its different arguments.I also learnt that -k argument is used to search.

## References 
None.
