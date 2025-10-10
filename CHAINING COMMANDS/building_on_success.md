# Building on success

In this challenge we need to chain the programs /challenge/first-success and /challenge/second using the && operator.

## My solve
**Flag:** ``

As the challenge suggests we can chain the commands with && in order to get the flag.

```
hacker@chaining~building-on-success:~$ /challenge/first-success
hacker@chaining~building-on-success:~$ /challenge/second
Error: /challenge/first-success must be successfully chained with 
/challenge/second using &&
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{07jt7aVH5i0uj9k9npMv4i9JEIu.0lM0MDOxwiM1kjNzEzW}
```

## What I learned

I learnt that we can also chain commands with && but && runs the second command only when the first one is executed 
successfully.

## References 
None.
