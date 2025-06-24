# information
##### Tags
Easy\
Forensics\
picoCTF 2021\
Author: susie
#### Description
> Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/7cf6a33f90deeeac5c73407a1bdc99b6/cat.jpg)
## Solution
Download the file and use `exiftool` to view the metadata.  `exiftool cat.jpg`

Either use the command line or CyberChef to undo the base64
`echo "<base64>" | base64 -d`

CyberChef Recipe:
```
From_Base64('A-Za-z0-9+/=',true,false)
```

### Flag
`picoCTF{t...d}`
