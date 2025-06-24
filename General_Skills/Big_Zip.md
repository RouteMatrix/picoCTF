# Big Zip
Easy
General Skills
picoGym Exclusive
Author: LT 'syreal' Jones
#### Description
> Unzip this archive and find the flag.  [Download zip file](https://artifacts.picoctf.net/c/505/big-zip-files.zip)
## Solution
Download and extract the zip file.  This zip file contains a lot of text files, and folders with more text files in them.  The easiest way to find the flag is using a bash for loop to grep each file for the flag.
```bash
for i in $(find . -name "*.txt"); do grep "picoCTF" $i; done
```

### Flag
`picoCTF{g...c}`
