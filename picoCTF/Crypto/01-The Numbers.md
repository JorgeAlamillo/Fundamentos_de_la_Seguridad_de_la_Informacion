### The Numbers
### Descripción

The numbers... what do they mean?[numbers.png](https://challenge-files.picoctf.net/c_fickle_tempest/7b39deba4212c233b1628c93f16639ed02ad90f51436d2a8914bb11f74a982d3/the_numbers.png)
### Solución

┌──(JorgeMSI㉿MSI)-[~/crypto/thenumbers]
└─$ wget https://challenge-files.picoctf.net/c_fickle_tempest/7b39deba4212c233b1628c93f16639ed02ad90f51436d2a8914bb11f74a982d3/the_numbers.png
--2026-04-13 12:06:55--  https://challenge-files.picoctf.net/c_fickle_tempest/7b39deba4212c233b1628c93f16639ed02ad90f51436d2a8914bb11f74a982d3/the_numbers.png
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.174.207.125, 3.174.207.109, 3.174.207.121, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.174.207.125|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 100721 (98K) [application/octet-stream]
Saving to: ‘the_numbers.png’

the_numbers.png               100%[=================================================>]  98.36K  --.-KB/s    in 0.05s

2026-04-13 12:06:56 (1.87 MB/s) - ‘the_numbers.png’ saved [100721/100721]


┌──(JorgeMSI㉿MSI)-[~/crypto/thenumbers]
└─$ ls
the_numbers.png

┌──(JorgeMSI㉿MSI)-[~/crypto/thenumbers]
└─$ open the_numbers.png

16 9 3 15 3 20 6 { 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14}

https://gchq.github.io/CyberChef/#recipe=A1Z26_Cipher_Decode('Space')&input=MTYgOSAzIDE1IDMgMjAgNiB7IDIwIDggNSAxNCAyMSAxMyAyIDUgMTggMTkgMTMgMSAxOSAxNSAxNCB9


picoctf{thenumbersmason}


### Notas
### Referencias