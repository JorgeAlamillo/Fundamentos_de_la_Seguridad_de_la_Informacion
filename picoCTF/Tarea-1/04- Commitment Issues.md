### ### Commitment Issues

### Descripción

I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/75/challenge.zip)
### Solución

### Solucion 1 - Usando Consola

```

JorgeAlamillo-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c_titan/75/challenge.zip
JorgeAlamillo-picoctf@webshell:~$ unzip challenge.zip 

JorgeAlamillo-picoctf@webshell:~$ ls
README.txt  challenge.zip  drop-in  home
JorgeAlamillo-picoctf@webshell:~$ cd drop-in/
JorgeAlamillo-picoctf@webshell:~/drop-in$ ls
message.txt
JorgeAlamillo-picoctf@webshell:~/drop-in$ cat message.txt 
TOP SECRET
JorgeAlamillo-picoctf@webshell:~/drop-in$ ls -la
total 12
drwxr-xr-x 3 JorgeAlamillo-picoctf JorgeAlamillo-picoctf   49 Mar  9  2024 .
drwxr-xr-x 7 JorgeAlamillo-picoctf JorgeAlamillo-picoctf 4096 Feb 21 02:36 ..
drwxr-xr-x 8 JorgeAlamillo-picoctf JorgeAlamillo-picoctf 4096 Mar  9  2024 .git
-rw-r--r-- 1 JorgeAlamillo-picoctf JorgeAlamillo-picoctf   11 Mar  9  2024 message.txt
JorgeAlamillo-picoctf@webshell:~/drop-in$ git log

JorgeAlamillo-picoctf@webshell:~/drop-in$ git show 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2

picoCTF{s@n1t1z3_9539be6b}

```

### Notas
- `ls -la` es un comando que sirve para listar todo el contenido de una carpeta con máximo detalle.
- `git log` es el historial de navegación de un proyecto de programación. 
- el Hash que puse en el `git show`  es la identificación única de ese cambio o commit.
