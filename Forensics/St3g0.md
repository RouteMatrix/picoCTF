# St3g0
Medium\
Forensics\
picoCTF 2022\
steganography\
Author: LT 'syreal' Jones (ft. djrobin17)
#### Description
Download this image and find the flag. [Download image](https://artifacts.picoctf.net/c/215/pico.flag.png)
## Solution
Download the file and after using `file` we see we have a PNG image file. 

Using [zsteg](https://github.com/zed-0xff/zsteg) to analyze the PNG file, we found the flag in one of the text fields.
```bash
zsteg pico.flag.png
```

### Flag
`picoCTF{7...}`
