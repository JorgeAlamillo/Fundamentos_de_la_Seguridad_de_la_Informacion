### GET aHEAD

### Descripción

Find the flag being held on this server to get ahead of the competitionhttp://wily-courier.picoctf.net:53972/
### Solución

### Solucion 1 usando Consola de Kali Linux

```
┌──(JorgeMSI㉿MSI)-[~]
└─$ curl -I HEAD http://wily-courier.picoctf.net:53972/index.php
curl: (6) Could not resolve host: HEAD
HTTP/1.1 200 OK
Date: Thu, 26 Feb 2026 01:40:59 GMT
Server: Apache/2.4.38 (Debian)
X-Powered-By: PHP/7.2.34
flag: picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
Content-Type: text/html; charset=UTF-8




```


### Notas
- Get: Se utiliza para obtener un recurso solo obtener datos.
- Post: Envia informacion al recurso a veces causando cambios al otro lado en el servidor.
- Head: identico al Get pero no hay respuesta.
### Referencias
- https://www.youtube.com/watch?v=oiZk0tIkR48&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=12