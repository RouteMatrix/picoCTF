# CanYouSee
##### Tags
Easy\
Forensics\
picoCTF 2024\
browser_webshell_solvable\
Author: Mubarak Mikail
#### Description
> How about some hide and seek? Download this file [here](https://artifacts.picoctf.net/c_titan/130/unknown.zip).
## Solution
After downloading and expanding the Zip file we find a file called `ukn_reality.jpg`, after checking with `file` it is in fact a JPG file.

Let's start with `exiftool`:


Well, most URL's don't look like base64, let's decode that.

`echo "<base64>" | base64 -d`

### Commands in Order
```bash
file ukn_reality.jpg
exiftool ukn_reality.jpg
echo "<base64> | base64 -d"
```

### Flag
`picoCTF{ME7...4}`
