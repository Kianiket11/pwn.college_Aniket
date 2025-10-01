# Deleting characters

In this challenge there are some decoy characters (specifically: ^ and %) among the flag characters. We have to remove them in order to
get the flag

## My solve
**Flag:** `pwn.college{wcbcpkfBhBkkMywuLn_jhKjjbx5.0FNxEzNxwiM1kjNzEzW}`

As the challenge suggests that there are some decoy characters specifically ^ and %. What we can do to remove them is use the tr
command with -d which is used to delete characters that are given in the argument. Now i used "flag" | tr -d ^% to get the flag.

```
hacker@data~deleting-characters:~$ /challenge/run
Your character-stuffed flag:
p^w^%n^.^%co^%l^l^e%ge^%{^%w^%c%b^%cp%k%f%B%h^B^%k^%kM%y%w^%u%L^%n^%_^%jh%K%j%j^b^%x5%.^%0^%F%N^%x^E^%zN^%x^%w^%i^%M^1^%k^j^%N^%z^E^z^W}%^%
hacker@data~deleting-characters:~$ echo p^w^%n^.^%co^%l^l^e%ge^%{^%w^%c%b^%cp%k%f%B%h^B^%k^%kM%y%w^%u%L^%n^%_^%jh%K%j%j^b^%x5%.^%0^%F%N^%x^E^%zN^%x^%w^%i^%M^1^%k^j^%N^%z^E^z^W}%^% | tr -d ^%
pwn.college{wcbcpkfBhBkkMywuLn_jhKjjbx5.0FNxEzNxwiM1kjNzEzW}
```

## What I learned

I learnt that we can use tr command -d to delete characters.

## References 
None.
