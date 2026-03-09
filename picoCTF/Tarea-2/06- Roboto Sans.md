### Roboto Sans

### Descripción

The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:63066/) out.

### Solución

- Abrimos la pagina
- Agregamos en el link el robots.txt : http://saturn.picoctf.net:63066/robots.txt
- nos aparece los siguiente
```
  User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
```
- Sabemos que las cadenas que terminan en == son clara codificacion de base 64
- Decodificamos la siguiente cadena anMvbXlmaWxlLnR4dA==
```
echo "anMvbXlmaWxlLnR4dA==" | base64 -d
```
- El resultado es js/myfile.txt
- lo ponemos en el link original http://saturn.picoctf.net:63066/js/myfile.txt
- Tenemos la bandera: picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}
