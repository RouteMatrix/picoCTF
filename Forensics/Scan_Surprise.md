# Scan Surprise
##### Tags
Easy\
Forensics\
picoCTF 2024\
shellbrowser_webshell_solvable\
qr_code\
Author: Jeffery John
#### Description
> I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here: [challenge.zip](https://artifacts.picoctf.net/c_atlas/2/challenge.zip)
## Solution
After downloading and expanding the Zip file we have a PNG file.  Once the file is loaded it is a QR code.  Let's install a command line tool `zbarimg` that will print out the text of the QR code.

Install:\
`sudo apt install zbar-tools`

Get the Flag:\
`zbarimg flag.png`
### Command List
```bash
file flag.png
sudo apt install zbar-tools
zbar-tools flag.png
```

### Flag
`picoCTF{p...2}`
