
# Transformation

- `#ReverseEngineering`
- I wonder what this really is `enc' '.join( [chr( (ord(flag[i]) << 8) + ord(flag[i +1])) for i in range(0,len(flag), 2)])'`
- hint: find some decoders online
- `https://mercury.picoctf.net/static/a757282979af14ab5ed74f0ed5e2ca95/enc`
- `cat enc` and shows Chinese characters
- `picoCTF{16_bits_inst34d_of_8_d52c6b93}`