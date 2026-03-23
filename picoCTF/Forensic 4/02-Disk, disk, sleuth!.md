### Disk, disk, sleuth!

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image.[dds1-alpine.flag.img.gz](https://challenge-files.picoctf.net/c_wily_courier/a118330a1c5e12f3b59fc45a75b8838700482f89c8ea71a28aa1bd66c7ba3968/dds1-alpine.flag.img.gz)
### Solución
```
wget -q image.[dds1-alpine.flag.img.gz](https://challenge-files.picoctf.net/c_wily_courier/a118330a1c5e12f3b59fc45a75b8838700482f89c8ea71a28aa1bd66c7ba3968/dds1-alpine.flag.img.gz)
```

```
gunzip dds1-alpine.flag.img.gz
```

```
srch_strings dds1-alpine.flag.img | grep "picoCTF{"
```

┌──(JorgeMSI㉿MSI)-[~]
└─$ srch_strings dds1-alpine.flag.img | grep "picoCTF{"
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_5e56e786}
### Notas

### Referencias
