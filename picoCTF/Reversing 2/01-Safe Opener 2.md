### Safe Opener 2
### Descripción

What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/286/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
### Solución

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/01]
└─$ wget https://artifacts.picoctf.net/c/286/SafeOpener.class
--2026-05-07 10:11:33--  https://artifacts.picoctf.net/c/286/SafeOpener.class
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.125, 13.225.222.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2036 (2.0K) [application/octet-stream]
Saving to: ‘SafeOpener.class’

SafeOpener.class              100%[=================================================>]   1.99K  --.-KB/s    in 0s

2026-05-07 10:11:33 (21.0 MB/s) - ‘SafeOpener.class’ saved [2036/2036]


┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/01]
└─$ file SafeOpener2.class
SafeOpener2.class: cannot open `SafeOpener2.class' (No such file or directory)

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/01]
└─$ file SafeOpener.class
SafeOpener.class: compiled Java class data, version 52.0 (Java 1.8)

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/01]
└─$ strings SafeOpener.class | grep "picoCTF"

picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_3dae8463}
### Notas
### Referencias
