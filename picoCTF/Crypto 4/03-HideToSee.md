### HideToSee

### Descripción

How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/241/atbash.jpg).
### Solución

┌──(JorgeMSI㉿MSI)-[~/picoCTF/Crypto4/hidetosee]
└─$ wget https://artifacts.picoctf.net/c/241/atbash.jpg

┌──(JorgeMSI㉿MSI)-[~/picoCTF/Crypto4/hidetosee]
└─$ open atbash.jpg

┌──(JorgeMSI㉿MSI)-[~/picoCTF/Crypto4/hidetosee]
└─$ sudo apt install steghide

┌──(JorgeMSI㉿MSI)-[~/picoCTF/Crypto4/hidetosee]
└─$ steghide --extract -sf atbash.jpg
Enter passphrase:
wrote extracted data to "encrypted.txt".

┌──(JorgeMSI㉿MSI)-[~/picoCTF/Crypto4/hidetosee]
└─$ ls
atbash.jpg  encrypted.txt

┌──(JorgeMSI㉿MSI)-[~/picoCTF/Crypto4/hidetosee]
└─$ open encrypted.txt

┌──(JorgeMSI㉿MSI)-[~/picoCTF/Crypto4/hidetosee]
└─$ cat encrypted.txt

krxlXGU{zgyzhs_xizxp_7142uwv9}

https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher()&input=a3J4bFhHVXt6Z3l6aHNfeGl6eHBfNzE0MnV3djl9

picoCTF{atbash_crack_7142fde9}

### Notas
### Referencias
