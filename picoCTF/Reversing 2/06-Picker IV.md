### Picker IV
### Descripción

Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 60445`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/526/picker-III.py).
### Solución

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/06]
└─$ wget https://artifacts.picoctf.net/c/529/picker-IV.c
--2026-05-07 10:38:48--  https://artifacts.picoctf.net/c/529/picker-IV.c
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.105, 13.225.222.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 839 [application/octet-stream]
Saving to: ‘picker-IV.c’

picker-IV.c                   100%[=================================================>]     839  --.-KB/s    in 0s

2026-05-07 10:38:49 (9.72 MB/s) - ‘picker-IV.c’ saved [839/839]


┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/06]
└─$ wget https://artifacts.picoctf.net/c/529/picker-IV
--2026-05-07 10:39:00--  https://artifacts.picoctf.net/c/529/picker-IV
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.105, 13.225.222.28, 13.225.222.125, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.105|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17272 (17K) [application/octet-stream]
Saving to: ‘picker-IV’

picker-IV                     100%[=================================================>]  16.87K  --.-KB/s    in 0.004s

2026-05-07 10:39:01 (4.52 MB/s) - ‘picker-IV’ saved [17272/17272]


┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/06]
└─$ chmod +x picker-IV

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/06]
└─$ ls
picker-IV  picker-IV.c

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/06]
└─$ nm picker-IV | grep win
000000000040129e T win

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/06]
└─$ nc saturn.picoctf.net 54910
Enter the address in hex to jump to, excluding '0x': 40129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_b8de1af4}


### Notas
### Referencias
