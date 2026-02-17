### PW Crack 1

### Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.
### Solución

### Solucion 1 - Usando Consola

```
wget -q https://artifacts.picoctf.net/c/12/level1.py 
wget -q https://artifacts.picoctf.net/c/12/level1.flag.txt.enc

nano level1.py
"abrimos para ver la contrasena, la contrasena es 8713"

JorgeAlamillo-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}

```

