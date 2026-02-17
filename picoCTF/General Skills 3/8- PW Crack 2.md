### PW Crack 1

### Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
### Solución

### Solucion 1 - Usando Consola

```
 wget -q https://artifacts.picoctf.net/c/13/level2.py
JorgeAlamillo-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
JorgeAlamillo-picoctf@webshell:~$ nano level2.py
"entramos al codigo y vemos la contrasena, y la convertimos"
JorgeAlamillo-picoctf@webshell:~$ python
>>> chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36)
'de76'
>>> exit()
JorgeAlamillo-picoctf@webshell:~$ python level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}

```

