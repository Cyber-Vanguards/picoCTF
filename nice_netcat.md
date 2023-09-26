
# Nice Netcat

- `#general-skills`
- There is a nice program that you can talk to by using this command in a shell but it doesn't speak English
- `nc mercury.picoctf.net 21135`
- hint: practice reading & writing ASCII 
- run `nc mercury.picoctf.net 21135 | tr -d '\n' >> netcat.txt` which removes newlines
- `cat netcat.txt` and see numeric values
- search decimal to ASCII converter, copy numbers 
- `https://www.rapidtables.com/convert/number/ascii-hex-bin-dec-converter.html` and paste in numbers in Decimal section
- `picoCTF{g00d_k1tty!_n1c3_k1tty!_afd5fda4}`