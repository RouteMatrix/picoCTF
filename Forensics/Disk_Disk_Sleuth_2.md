# Disk, disk, sleuth! II
Medium\
Forensics\
picoCTF 2021\
Author: syreal
#### Description
All we know is the file with the flag is named `down-at-the-bottom.txt`... Disk image: dds2-alpine.flag.img.gz
## Solution
Download and unzip the gunzip file.  Using the `mmls` we can find the start point of the linux partition.
```bash
mmls dds2-alpine.flag.img
```
Next we can start looking for the file.  `fls` has 2 options that allow us to display the full file and recursively list the directory entries.  Combining this with `grep` we should be able to locate the file fast. 

`fls -r -p -o 2048 dds2-alpine.flag.img | grep down-at-the-bottom.txt`\

Lets output that text file to the local system:

`icat -o 2048 dds2-alpine.flag.img 18291`\

`cat down-at-the-bottom.txt`\

### Flag
```
picoCTF{f...d}
```
