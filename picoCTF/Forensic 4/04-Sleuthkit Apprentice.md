### Sleuthkit Apprentice
### Descripción

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/136/disk.flag.img.gz)
### Solución

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ wget https://artifacts.picoctf.net/c/136/disk.flag.img.gz
--2026-03-23 11:02:45--  https://artifacts.picoctf.net/c/136/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 47534571 (45M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz.2’

disk.flag.img.gz.2            100%[=================================================>]  45.33M   582KB/s    in 88s

2026-03-23 11:04:17 (528 KB/s) - ‘disk.flag.img.gz.2’ saved [47534571/47534571]


┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ gunzip disk.flag.img.gz

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ icat -i raw -f ext4 -o 360448 disk.flag.img 2082
            3.449677            13.056403

┌──(JorgeMSI㉿MSI)-[/tmp]
└─$ icat -i raw -f ext4 -o 360448 disk.flag.img 2371
picoCTF{by73_5urf3r_3497ae6b}
