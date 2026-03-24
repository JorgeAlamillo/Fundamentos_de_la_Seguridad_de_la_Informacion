### CanYouSee

### Descripción

How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/130/unknown.zip).
### Solución

──(JorgeMSI㉿MSI)-[~/canyousee]
└─$ ls
unknown.zip.gz

┌──(JorgeMSI㉿MSI)-[~/canyousee]
└─$ gunzip unknown.zip.gz

┌──(JorgeMSI㉿MSI)-[~/canyousee]
└─$ ls
unknown.zip

┌──(JorgeMSI㉿MSI)-[~/canyousee]
└─$ unzip unknown.zip
Archive:  unknown.zip
  inflating: ukn_reality.jpg

┌──(JorgeMSI㉿MSI)-[~/canyousee]
└─$ ls
ukn_reality.jpg  unknown.zip

┌──(JorgeMSI㉿MSI)-[~/canyousee]
└─$ exiftool ukn_reality.jpg

Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg==

┌──(JorgeMSI㉿MSI)-[~/canyousee]
└─$ echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg = =" | base64 -d

picoCTF{ME74D47A_HIDD3N_6a9f5ac4}


### Notas
### Referencias