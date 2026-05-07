### Picker III
### Descripción

Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 60445`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/526/picker-III.py).
### Solución


┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/05]
└─$ wget https://artifacts.picoctf.net/c/526/picker-III.py
--2026-05-07 10:29:34--  https://artifacts.picoctf.net/c/526/picker-III.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.105, 13.225.222.125, 13.225.222.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.105|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4439 (4.3K) [application/octet-stream]
Saving to: ‘picker-III.py’

picker-III.py                 100%[=================================================>]   4.33K  --.-KB/s    in 0s

2026-05-07 10:29:34 (56.9 MB/s) - ‘picker-III.py’ saved [4439/4439]

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/05]
└─$ nc saturn.picoctf.net 60445
==> 3
Please enter variable name to write: func_table
Please enter new value of variable: 'win' + ' ' * 29 + 'a' * 96
==> 1
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x37 0x68 0x31 0x35 0x5f 0x31 0x35 0x5f 0x77 0x68 0x34 0x37 0x5f 0x77 0x33 0x5f 0x67 0x33 0x37 0x5f 0x77 0x31 0x37 0x68 0x5f 0x75 0x35 0x33 0x72 0x35 0x5f 0x31 0x6e 0x5f 0x63 0x68 0x34 0x72 0x67 0x33 0x5f 0x32 0x32 0x36 0x64 0x64 0x32 0x38 0x35 0x7d
==> python3 -c "print(bytes.fromhex('70 69 63 6f 43 54 46 7b 37 68 31 35 5f 31 35 5f 77 68 34 37 5f 77 33 5f 67 33 37 5f^C                                                                                                                     "

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/05]
└─$ python3 -c "print(bytes.fromhex('70 69 63 6f 43 54 46 7b 37 68 31 35 5f 31 35 5f 77 68 34 37 5f 77 33 5f 67 33 37 5f 77 31 37 68 5f 75 35 33 72 35 5f 31 6e 5f 63 68 34 72 67 33 5f 32 32 36 64 64 32 38 35 7d'.replace(' ', '')).decode())"
picoCTF{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_226dd285}

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/05]
└─$

### Notas
### Referencias
