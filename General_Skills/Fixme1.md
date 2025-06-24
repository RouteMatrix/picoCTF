# fixme1.py
Easy\
General Skills\
Beginner picoMini 2022\
Python\
Author: LT 'syreal' Jones
#### Description
> Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
## Solution
After downloading the file and loading the Python script into Visual Studio Code, install the Python Extension certified by Microsoft.

Once the extension is loaded, errors will be highlighted automatically.  On line 20, remove the leading spaces for the print statement.

Run the script on the command line for the flag.
```bash
python3 fixme1.py
```
### Flag
`picoCTF{1...f}`
