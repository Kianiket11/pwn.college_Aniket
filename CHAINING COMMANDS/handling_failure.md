# Handling failure 

In this challenge we need to chain /challenge/first-failure and /challenge/second using the || operator. 

## My solve
**Flag:** `pwn.college{Q3CwIanx2msdQvBE5CnlFdN9YK6.01M0MDOxwiM1kjNzEzW}`

As the challenge suggests we can chain commands with || in order to get the flag.

```
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{Q3CwIanx2msdQvBE5CnlFdN9YK6.01M0MDOxwiM1kjNzEzW}

```

## What I learned

I learnt that || can be used to chain commands but what || means is "Run command1, and If it fails, then run command2."

## References 
None.
