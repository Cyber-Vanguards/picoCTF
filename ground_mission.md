
# ground mission

- `#general-skills`
- Do you know how to move between directories and read files in the shell? Start the container `ssh` to it and `ls` once connected. Login via `ssh` as `ctf-player` with the password `a13b7f9d`
- launch instance, `ssh ctf-player@venus.picoctf.net -p 56969`
- copy ssh command in terminal, paste password
- `cat instructions-to-2of3.txt`
- `cat 1of3.flag.txt`  = `picoCTF{xxsh_`
- `cd /`  , `ls`
- `cat 2of3.flag.txt` = `0ut_0f_\/\/4t3r`
- `cat instructions-to-3of3.txt` 
- `cd ~`
- `cat 3of3.flag.txt` = `71be5264}`
- `picoCTF{xxsh_0ut_0f_\/\/4t3r_71be5264}`