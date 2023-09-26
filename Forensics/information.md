
# Information

- `#Forensics`
- Files can always be changed in a secret way, can you find the flag?
- file: `https://mercury.picoctf.net/static/e5825f58ef798fdd1af3f6013592a971/cat.jpg`
- hint: look at the details of the file
- open image to see what it has
- `exiftool cat.jpg` and see for License:  `cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9`
- terminal: `echo <paste string> | base64 -d > cat-flag.txt`
- `picoCTF{the_m3tadata_1s_modified}` 