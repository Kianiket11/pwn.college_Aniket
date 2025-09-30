# Deleting characters


## My solve
**Flag:** `pwn.college{wcbcpkfBhBkkMywuLn_jhKjjbx5.0FNxEzNxwiM1kjNzEzW}`


```
hacker@data~deleting-characters:~$ /challenge/run
Your character-stuffed flag:
p^w^%n^.^%co^%l^l^e%ge^%{^%w^%c%b^%cp%k%f%B%h^B^%k^%kM%y%w^%u%L^%n^%_^%jh%K%j%j^b^%x5%.^%0^%F%N^%x^E^%zN^%x^%w^%i^%M^1^%k^j^%N^%z^E^z^W}%^%
hacker@data~deleting-characters:~$ echo p^w^%n^.^%co^%l^l^e%ge^%{^%w^%c%b^%cp%k%f%B%h^B^%k^%kM%y%w^%u%L^%n^%_^%jh%K%j%j^b^%x5%.^%0^%F%N^%x^E^%zN^%x^%w^%i^%M^1^%k^j^%N^%z^E^z^W}%^% | tr -d ^%
pwn.college{wcbcpkfBhBkkMywuLn_jhKjjbx5.0FNxEzNxwiM1kjNzEzW}
```

## What I learned


## References 
None.
