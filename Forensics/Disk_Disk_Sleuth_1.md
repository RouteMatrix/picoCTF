# Disk, disk, sleuth!
##### Tags
Medium\
Forensics\
picoCTF 2021\
Author: syreal
#### Description
> Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: dds1-alpine.flag.img.gz
## Solution
Download and unzip the gunzip file.  Use the `srch_strings` and pipe (`|`) the output to `grep` and search term _pico_.
```bash
srch_strings dds1-alpine.flag.img | grep pico
```
### Flag
`picoCTF{f...}`
