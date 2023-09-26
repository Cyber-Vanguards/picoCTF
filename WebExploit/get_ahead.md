
# Get aHead

- `#Web-Exploit`
- Find the flag being held on this server to get ahead of the competition
- `http://mercury.picoctf.net:34561/`
- hint = check out tools like Burpsuite to modify your requests & look at responses
- open browser and select 'choose red' and 'choose blue' , open developer tools Network tab
- 'select blue' is a POST request, 'select red' is a GET request
- click on red again, click on GET, right side corner click 'Resend', left side box has method GET with drop-down menu and choose HEAD and click send, click on HEAD inside the middle window box and see on 3rd window `flag`
- `picoCTF{r3j3ct_th3_du4l1ty_8f878508}`