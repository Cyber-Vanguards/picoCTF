
# matryoshka doll

- `#Forensics`
- Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. what's the final one?
- `https://mercury.picoctf.net/static/b6205dd933ec01c022c4e6acbdf11116/dolls.jpg`
- `file dolls.jpg` = PNG file
- `xxd dolls.jpg`  .PNG
- `mv dolls.jpg dolls.png` 
- `eom dolls.png`  (or `eog dolls.png`)
- `binwalk dolls.png`
- there is a hidden zip file inside, `unzip dolls.png` outputs `base_images/2_c.jpg` cd into base_images and `binwalk 2_c.jpg` and see another zip file
- repeat process `base_images` and `unzip <file>`
- programmatic approach is to make inline script but first  go back and delete the base_images folder. just have dolls.png. `for i in {0..100}; do unzip *.jpg; cd base_images; done`
- `cd base_images/base_images/base_images/` and see 4_c.jpg and flag.txt
- `picoCTF{4f11048e83ffc7d342a15bd2309b47de}`