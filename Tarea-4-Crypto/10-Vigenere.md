### Vigenere
### Descripción

Can you decrypt this message?Decrypt this [message](https://artifacts.picoctf.net/c/158/cipher.txt) using this key "CYLAB".
### Solución

┌──(JorgeMSI㉿MSI)-[~/crypto/tarea4/10]
└─$ wget https://artifacts.picoctf.net/c/158/cipher.txt
--2026-04-27 20:40:27--  https://artifacts.picoctf.net/c/158/cipher.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.61, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 43 [application/octet-stream]
Saving to: ‘cipher.txt’

cipher.txt                    100%[=================================================>]      43  --.-KB/s    in 0s

2026-04-27 20:40:28 (15.7 MB/s) - ‘cipher.txt’ saved [43/43]


┌──(JorgeMSI㉿MSI)-[~/crypto/tarea4/10]
└─$ cat cipher.txt
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_cc82272b}

https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('CYLAB')&input=DQpyZ25vRFZEe08wTlVfV1EzX0cxRzNPM1QzX0ExQUgzU19jYzgyMjcyYn0&oenc=65001&ieol=CRLF&oeol=CRLF

picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_ae82272q}
### Notas
### Referencias
- Cyberchef