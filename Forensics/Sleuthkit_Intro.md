# Sleuthkit Intro
##### Tags
Medium\
Forensics\
picoCTF 2022\
sleuthkit\
Author: LT 'syreal' Jones
#### Description
> Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

> Access checker program: `nc saturn.picoctf.net 55735`
## Solution
Download and unzip the gunzip file.  Install the `mmls` by installing Sleuthkit: `sudo apt install sleuthkit`.  To see the partitions just load the image into `mmls`. After launching the instance (score server) connect with the supplied netcat `nc` and submit the partition Length.
```bash
mmls disk.img
nc saturn.picoctf.net 57246
# Enter: 202752
```
### Flag
`picoCTF{m...}`
