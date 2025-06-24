# Operation Orchid
##### Tags
Medium\
Forensics\
picoCTF 2022\
disk\
Author: LT 'syreal' Jones
#### Description
> Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.  [Download compressed disk image](https://artifacts.picoctf.net/c/212/disk.flag.img.gz)
## Solution
After downloading and extracting the Zip file we find the contained file of `disk.flag.img` which appears to be a DOS/MBR disk image.  
```bash
file disk.flag.img
```
Now we have to find the filesystem start with listing the partition tables:
```bash
mmls disk.flag.img
```
Partitions 0,1,2,3 are all very small, so listing out partition 4 is the likely scenario.
```bash
fls -o 411648 disk.flag.img
```
Looking in the `root` folder we find the `flag.txt` and `flag.txt.enc` files.
```bash
fls -o 411648 disk.flag.img 472
```

Flag.txt is not readable only `flag.txt.enc` is.  This means we need to find how to open the encrypted file.
```bash
icat disk.flag.img -o 411648 1876
icat disk.flag.img -o 411648 1782
```
Let's search the command history and see if we can find references to the `flag.txt`.
```bash
strings -t d disk.flag.img | grep flag.txt
```
Looks like we found the openssl command and the password used in the encryption process.   This matches the `flag.txt.enc` Salted file in the root directory let's export the encrypted file to our local system then decrypt.
```bash
icat disk.flag.img -o 411648 1782 > flag.txt.enc
openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k <password>
cat flag.txt
```
#### Command list
```bash
 gunzip disk.flag.img.gz 
 mmls disk.flag.img 
 fls -o 411648 disk.flag.img 
 fls -o 411648 disk.flag.img 472
 strings -t d disk.flag.img | grep flag.txt
 icat disk.flag.img -o 411648 1782 > flag.txt.enc
 openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k <password>
 cat flag.txt
```

### Flag
`picoCTF{h...5}`
