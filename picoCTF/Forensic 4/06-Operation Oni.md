### Operation Oni

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image.[dds1-alpine.flag.img.gz](https://challenge-files.picoctf.net/c_wily_courier/a118330a1c5e12f3b59fc45a75b8838700482f89c8ea71a28aa1bd66c7ba3968/dds1-alpine.flag.img.gz)
### Solución
┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ ls
disk.img.gz

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ file disk.img.gz
disk.img.gz: gzip compressed data, was "disk.img", last modified: Wed Oct  6 14:32:01 2021, from Unix, original size modulo 2^32 241172480

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ gunzip disk.img.gz

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ ls
disk.img

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ file disk.img
disk.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,223,19), startsector 2048, 204800 sectors; partition 2 : ID=0x83, start-CHS (0xc,223,20), end-CHS (0x1d,81,52), startsector 206848, 264192 sectors

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ fsstat -o 2048 disk.img

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ fls -o 2048 disk.img
V/V 25585:      $OrphanFiles

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ fls -o 206848 disk.img
d/d 470:        root

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ fls -o 206848 disk.img 470
r/r 2344:       .ash_history
d/d 3916:       .ssh

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ fls -o 206848 disk.img 3916
r/r 2345:       id_ed25519
r/r 2346:       id_ed25519.pub

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ icat -o 206848 disk.img 2345
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ icat -o 206848 disk.img 2346

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ icat -o 206848 disk.img 2345 > id_ed25519

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ ls
disk.img  id_ed25519

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ ls -l id_ed25519
-rw-r--r-- 1 JorgeMSI JorgeMSI 411 Mar 23 10:36 id_ed25519

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ chmod 600 id_ed25519

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ ls -al
total 235532
drwxr-xr-x  2 JorgeMSI JorgeMSI      4096 Mar 23 10:36 .
drwx------ 33 JorgeMSI JorgeMSI      4096 Mar 23 10:30 ..
-rw-r--r--  1 JorgeMSI JorgeMSI 241172480 Aug  4  2023 disk.img
-rw-------  1 JorgeMSI JorgeMSI       411 Mar 23 10:36 id_ed25519

┌──(JorgeMSI㉿MSI)-[~/oni]
└─$ ssh -i id_ed25519 -p 53003 ctf-player@saturn.picoctf.net


ctf-player@challenge:~$ cat flag.txt
picoCTF{k3y_5l3u7h_b5066e83}

### Notas

### Referencias
