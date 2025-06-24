# extensions
Medium\
Forensics\
picoCTF 2019\
Author: Sanjay C/Danny
#### Description
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Solution
Download the file and run the `file` command.  
`file flag.txt`

Seeing the file is actually a png we can open this file in `eog`.

`eog flag.txt`
### Flag
`picoCTF{n...s}`
