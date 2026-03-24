### Secret of the Polyglot
### Descripción

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/99/flag2of2-final.pdf).
### Solución

┌──(JorgeMSI㉿MSI)-[~/polyglot]
└─$ wget https://artifacts.picoctf.net/c_titan/99/flag2of2-final.pdf
--2026-03-23 19:24:12--  https://artifacts.picoctf.net/c_titan/99/flag2of2-final.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.26, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3362 (3.3K) [application/octet-stream]
Saving to: ‘flag2of2-final.pdf’

flag2of2-final.pdf            100%[=================================================>]   3.28K  --.-KB/s    in 0s

2026-03-23 19:24:13 (188 MB/s) - ‘flag2of2-final.pdf’ saved [3362/3362]


┌──(JorgeMSI㉿MSI)-[~/polyglot]
└─$ ls
flag2of2-final.pdf

┌──(JorgeMSI㉿MSI)-[~/polyglot]
└─$ file flag2of2-final.pdf
flag2of2-final.pdf: PNG image data, 50 x 50, 8-bit/color RGBA, non-interlaced

┌──(JorgeMSI㉿MSI)-[~/polyglot]
└─$ cp flag2of2-final.pdf parte1.png

┌──(JorgeMSI㉿MSI)-[~/polyglot]
└─$ ls
flag2of2-final.pdf  parte1.png

┌──(JorgeMSI㉿MSI)-[~/polyglot]
└─$ extension .
extension: command not found

┌──(JorgeMSI㉿MSI)-[~/polyglot]
└─$ explorer.exe .

Abrimos los dos archivos y juntamos la bandera

picoCTF{f1u3n7_1n_pn9_&_pdf_2a6a1ea8}

### Notas
### Referencias