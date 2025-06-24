# Wave a flag
Easy\
General Skills\
picoCTF 2021\
Author: syreal
#### Description
> Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm) has extraordinarily helpful information...
## Solution
There are two ways to solve this.
### First
Make the ELF binary executable by changing the permissions.  Then call the program with the help flag `./warm -h`.
```bash
chmod +x warm
./warm -h
```

### Second
The second option is to use `strings` and `grep`.
```bash
strings warm | grep "picoCTF"
```

### Flag
`picoCTF{b...a}`
