
# tunn3lv1s10n

- `#Forensics`
- We found this file, recover the flag
- `https://mercury.picoctf.net/static/7b2d7c26630e977197022d0af09e3aeb/tunn3l_v1s10n`
- `file tunn3l_v1s10n` data
- `strings tunn3l_v1s10n | grep picoCTF` no results
- open file through a hex editor `xxd tunn3l_v1s10n`  scroll to the top of output and see `BM.&` BM meaning bitmap 
- change file extension `tunn3l_v1s10n.bmp`
- `sudo apt install steghide -y` , `which steghide` shows directory path
- `sudo apt install ghex` and open `ghex` and open the `.bmp` file and open a regular BMP image file and compare. the top row has `BA` `D0`, change to 36 28. open file and see a `notaflag{sorry}` 
- run `exiftool tunn3l_v1s10n.bmp` , the image dimensions are weird (1134 x 306)
- `python3 hex(1134)` = `0x46e` , `hex(306)` = `0x132`
- the values for this BMP file were reversed so `hex(850)` = `0x352` is the proper value, edit the hex in the `ghex` to have in 6th 7th columns `52 03` save file, open BMP 
- `picoCTF{qu1t3_a_v13w_2020}`