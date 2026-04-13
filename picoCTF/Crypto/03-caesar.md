### caesar
### Descripción

Decrypt this message.Message: [message](https://challenge-files.picoctf.net/c_fickle_tempest/416ba12d66a8544f2d97e21fb165aa02f99c01ea26c5cec454a98c24c2e538d0/data.enc)
### Solución

┌──(JorgeMSI㉿MSI)-[~/crypto/caesar]
└─$ wget https://challenge-files.picoctf.net/c_fickle_tempest/416ba12d66a8544f2d97e21fb165aa02f99c01ea26c5cec454a98c24c2e538d0/data.enc
--2026-04-13 12:15:53--  https://challenge-files.picoctf.net/c_fickle_tempest/416ba12d66a8544f2d97e21fb165aa02f99c01ea26c5cec454a98c24c2e538d0/data.enc
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.174.207.125, 3.174.207.96, 3.174.207.121, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.174.207.125|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 36 [application/octet-stream]
Saving to: ‘data.enc’

data.enc                      100%[=================================================>]      36  --.-KB/s    in 0s

2026-04-13 12:15:54 (12.6 MB/s) - ‘data.enc’ saved [36/36]


┌──(JorgeMSI㉿MSI)-[~/crypto/caesar]
└─$ ls
data.enc

┌──(JorgeMSI㉿MSI)-[~/crypto/caesar]
└─$ cat data.enc
picoCTF{mbyccsxqdrobelsmyxigfknnoo}

https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,16)&input=bWJ5Y2NzeHFkcm9iZWxzbXl4aWdma25ub28

picoCTF{crossingtherubiconywvaddee}



### Notas
### Referencias