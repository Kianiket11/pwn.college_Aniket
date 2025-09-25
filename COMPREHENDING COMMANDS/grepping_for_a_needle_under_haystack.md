# Grepping for a needle in a haystack

In this challenge we have to use the grep command to find the flag from the hundred thousand lines of text in
the /challenge/data.txt file. hint: The flag always starts with the text pwn.college.


## My solve
**Flag:** `pwn.college{IErDNKyxVVRGBeeMGuaF95Zec6g.QX3EDO0wiM1kjNzEzW}`

As we have to search for the flag, we'll be using grep command to do so. the command we can use is 
grep pwn.college /challenge/data.txt. here grep will search the file for lines of text containing pwn.college(search_string)
and print them to the console.

```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{IErDNKyxVVRGBeeMGuaF95Zec6g.QX3EDO0wiM1kjNzEzW}
```

## What I learned
I learnt about the grep command and how to use this command for searching a particular file or a particular string in a particular
file. grep is a very efficient command compared to cat when it comes to large files/texts. 

## References 
None.

