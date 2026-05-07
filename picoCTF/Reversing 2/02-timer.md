### timer
### Descripción

You will find the flag after analysing this apkDownload [here](https://artifacts.picoctf.net/c/449/timer.apk).
### Solución
┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2]
└─$ mkdir 02

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2]
└─$ cd 02

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/02]
└─$ wget https://artifacts.picoctf.net/c/449/timer.apk
--2026-05-07 10:15:30--  https://artifacts.picoctf.net/c/449/timer.apk
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.120, 13.225.222.125, 13.225.222.105, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4678467 (4.5M) [application/octet-stream]
Saving to: ‘timer.apk’

timer.apk                     100%[=================================================>]   4.46M  5.07MB/s    in 0.9s

2026-05-07 10:15:32 (5.07 MB/s) - ‘timer.apk’ saved [4678467/4678467]


┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/02]
└─$ zgrep -a "picoCTF{" timer.apk

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/02]
└─$ cd timer_unzipped

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/02/timer_unzipped]
└─$ grep -r "picoCTF" .
grep: ./classes3.dex: binary file matches

┌──(JorgeMSI㉿MSI)-[~/picoCTF/reversing2/02/timer_unzipped]
└─$ strings classes3.dex | grep "picoCTF"
*picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}
### Notas
### Referencias
