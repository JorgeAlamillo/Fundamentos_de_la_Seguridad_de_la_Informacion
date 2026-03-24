### hideme
### Descripción

Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/262/flag.png).
### Solución

┌──(JorgeMSI㉿MSI)-[~/hideme]
└─$ wget https://artifacts.picoctf.net/c/262/flag.png
--2026-03-23 19:39:55--  https://artifacts.picoctf.net/c/262/flag.png
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.100, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 42945 (42K) [application/octet-stream]
Saving to: ‘flag.png’

flag.png                      100%[=================================================>]  41.94K  --.-KB/s    in 0.06s

2026-03-23 19:39:55 (661 KB/s) - ‘flag.png’ saved [42945/42945]


┌──(JorgeMSI㉿MSI)-[~/hideme]
└─$ file flag.png
flag.png: PNG image data, 512 x 504, 8-bit/color RGBA, non-interlaced

┌──(JorgeMSI㉿MSI)-[~/hideme]
└─$ binwalk flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2884, uncompressed size: 3038, name: secret/flag.png
42923         0xA7AB          End of Zip archive, footer length: 22


┌──(JorgeMSI㉿MSI)-[~/hideme]
└─$ binwalk -e flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2884, uncompressed size: 3038, name: secret/flag.png

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented


┌──(JorgeMSI㉿MSI)-[~/hideme]
└─$ ls
flag.png  _flag.png.extracted

┌──(JorgeMSI㉿MSI)-[~/hideme]
└─$ cd _flag.png.extracted

┌──(JorgeMSI㉿MSI)-[~/hideme/_flag.png.extracted]
└─$ ls -lh
total 52K
-rw-r--r-- 1 JorgeMSI JorgeMSI    0 Mar 23 19:40 29
-rw-r--r-- 1 JorgeMSI JorgeMSI  42K Mar 23 19:40 29.zlib
-rw-r--r-- 1 JorgeMSI JorgeMSI 3.2K Mar 23 19:40 9B3B.zip
drwxr-xr-x 2 JorgeMSI JorgeMSI 4.0K Mar 15  2023 secret

┌──(JorgeMSI㉿MSI)-[~/hideme/_flag.png.extracted]
└─$ cd secret/

┌──(JorgeMSI㉿MSI)-[~/hideme/_flag.png.extracted/secret]
└─$ ls
flag.png

┌──(JorgeMSI㉿MSI)-[~/hideme/_flag.png.extracted/secret]
└─$ explorer.exe flag.png

picoCTF{Hiddinng_An_imag3_within_@n_ima9e_82101824}
### Notas
### Referencias