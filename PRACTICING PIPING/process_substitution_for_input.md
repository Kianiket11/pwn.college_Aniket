# Process substitution for input

In this challenge we need to diff two sets of command outputs: /challenge/print_decoys, which will print a bunch of 
decoy flags, and /challenge/print_decoys_and_flag which will print those same decoys plus the real flag

## My solve
**Flag:** `pwn.college{0TvS4QTLb9ntXr3QSwmd3rHLwHD.0lNwMDOxwiM1kjNzEzW}`

As the challenge suggests we need to use the diff command which we learnt in previous module. here i used the concept of 
process substitution with diff in order to get the flag.

```
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
96a97
> pwn.college{0TvS4QTLb9ntXr3QSwmd3rHLwHD.0lNwMDOxwiM1kjNzEzW}
```

## What I learned

I learn that Linux follows the philosophy that "everything is a file". Then i learnt the concept of process substitution. 
Which can be initiated by <(command), when inititated , bash will run the command and hook up its output to a temporary 
file that it will create.

## References 
None.
