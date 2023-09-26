
# Static ain't always noise

- `#general-skills`
- Can you look at the data in this binary static? This BASH script might help
- `https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static`
- `https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh`
- `file static` is a ELF 64-bit executable
- `chmod +x ltdis.sh` 
- `nano ltdis.sh` check what it does
- run `./ltdis.sh`
- `./ltdis.sh static` will generate text files
- `nano  static.ltdis.x86_64.txt` to look at the Assembly language code
- `chmod +x static`  run `./static` get a clue printed out
- `nano static.ltdis.strings.txt` and see the flag 
- OR `strings static | grep picoCTF` and see the flag
- `picoCTF{d15a5m_t34s3r_6f8c8200}`