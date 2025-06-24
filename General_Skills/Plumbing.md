# plumbing
Medium\
General Skills\
picoCTF 2019\
Author: Alex Fulton/Danny Tunitis
#### Description
> Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 7480`.
## Solution
Using netcat `nc` to connect to the server and port we have a lot of output stating this isn't the flag etc....

Let's save the output to a file and grep for the flag.
```bash
nc jupiter.challenges.picoctf.org 7480 > plumbing.output
grep "picoCTF" plumbing.output
```

### Flag
`picoCTF{d...4}`
