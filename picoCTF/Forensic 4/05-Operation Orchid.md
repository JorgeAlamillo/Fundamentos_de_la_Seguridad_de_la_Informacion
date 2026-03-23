### Operation Orchid
### Descripción
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/213/disk.flag.img.gz)
### Solución
┌──(JorgeMSI㉿MSI)-[~]
└─$ cd /tmp

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ wget https://artifacts.picoctf.net/c/213/disk.flag.img.gz
--2026-03-23 10:45:21--  https://artifacts.picoctf.net/c/213/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.26, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 44360922 (42M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz              100%[=================================================>]  42.31M   194KB/s    in 63s

2026-03-23 10:46:32 (688 KB/s) - ‘disk.flag.img.gz’ saved [44360922/44360922]


┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ file disk.flag.img.gz
disk.flag.img.gz: gzip compressed data, was "disk.flag.img", last modified: Thu Mar 16 01:57:09 2023, from Unix, original size modulo 2^32 419430400

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ gunzip disk.flag.img.gz

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ fls -o 2048 disk.flag.img
d/d 11: lost+found
r/r 12: ldlinux.sys
r/r 13: ldlinux.c32
r/r 15: config-virt
r/r 16: vmlinuz-virt
r/r 17: initramfs-virt
l/l 18: boot
r/r 20: libutil.c32
r/r 19: extlinux.conf
r/r 21: libcom32.c32
r/r 22: mboot.c32
r/r 23: menu.c32
r/r 14: System.map-virt
r/r 24: vesamenu.c32
V/V 25585:      $OrphanFiles

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ fls -o 411648 disk.flag.img
d/d 460:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 81: proc
d/d 82: dev
d/d 83: tmp
d/d 84: lib
d/d 87: var
d/d 96: usr
d/d 106:        bin
d/d 120:        sbin
d/d 466:        media
d/d 470:        mnt
d/d 471:        opt
d/d 472:        root
d/d 473:        run
d/d 475:        srv
d/d 476:        sys
d/d 2041:       swap
V/V 51001:      $OrphanFiles

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ fls -o 411648 disk.flag.img 472
r/r 1875:       .ash_history
r/r * 1876(realloc):    flag.txt
r/r 1782:       flag.txt.enc

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ icat -o 411648 disk.flag.img 1782
Salted__�ށ��e��B�J�c�$QE&$��4jM�KGeE�1�^Ȥ7� ���؎$�'%
┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ strings -t d disk.flag.img | grep flag.txt
218985524 flag.txt
218985540 flag.txt.enc
219964416 touch flag.txt
219964431 nano flag.txt
219964483 nano flag.txt
219964506 openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
219964588 shred -u flag.txt
303193140 flag.txt
303317044 flag.txt
303317060 flag.txt.enc
303328308 flag.txt
303328324 flag.txt.enc

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ icat -o 411648 disk.flag.img 1782 > flag.txt.enc

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
40E704B91E7E0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ cat flag.txt

picoCTF{h4un71ng_p457_5113beab}
### Notas
### Referencias