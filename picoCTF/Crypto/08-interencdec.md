### interencdec
### Descripción

Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/111/enc_flag).

### Solución

┌──(JorgeMSI㉿MSI)-[~/crypto/interencdec]
└─$ wget https://artifacts.picoctf.net/c_titan/111/enc_flag
--2026-04-13 12:39:19--  https://artifacts.picoctf.net/c_titan/111/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 73 [application/octet-stream]
Saving to: ‘enc_flag’

enc_flag                      100%[=================================================>]      73  --.-KB/s    in 0s

2026-04-13 12:39:20 (142 MB/s) - ‘enc_flag’ saved [73/73]


┌──(JorgeMSI㉿MSI)-[~/crypto/interencdec]
└─$ open enc_flag

┌──(JorgeMSI㉿MSI)-[~/crypto/interencdec]
└─$ ls
enc_flag

┌──(JorgeMSI㉿MSI)-[~/crypto/interencdec]
└─$ cat enc_flag
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6ZzVNR3N5TXpjNWZRPT0nCg==

┌──(JorgeMSI㉿MSI)-[~/crypto/interencdec]
└─$ echo "YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6ZzVNR3N5TXpjNWZRPT0nCg== " | base64 -d
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fQ=='

┌──(JorgeMSI㉿MSI)-[~/crypto/interencdec]
└─$ echo "d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fQ== " | base64 -d
wpjvJAM{jhlzhy_k3jy9wa3k_890k2379}
┌──(JorgeMSI㉿MSI)-[~/crypto/interencdec]
└─$

https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,19)&input=d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fQ&oenc=65001&ieol=CRLF&oeol=CRLF

picoCTF{caesar_d3cr9pt3d_890d2379}

### Notas
### Referencias