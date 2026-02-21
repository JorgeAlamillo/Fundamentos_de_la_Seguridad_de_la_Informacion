### Blame Game

### Descripción

Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/158/challenge.zip)
### Solución

### Solucion 1 - Usando Consola

```
JorgeAlamillo-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c_titan/158/challenge.zip
JorgeAlamillo-picoctf@webshell:~$ unzip challenge.zip 

JorgeAlamillo-picoctf@webshell:~$ ls
challenge.zip  drop-in
JorgeAlamillo-picoctf@webshell:~$ cd drop-in/
JorgeAlamillo-picoctf@webshell:~/drop-in$ ls
message.py
JorgeAlamillo-picoctf@webshell:~/drop-in$ cat message.py 
print("Hello, World!"
JorgeAlamillo-picoctf@webshell:~/drop-in$ ls -la
total 12
drwxr-xr-x 3 JorgeAlamillo-picoctf JorgeAlamillo-picoctf   48 Mar 12  2024 .
drwxr-xr-x 6 JorgeAlamillo-picoctf JorgeAlamillo-picoctf 4096 Feb 21 02:55 ..
drwxr-xr-x 8 JorgeAlamillo-picoctf JorgeAlamillo-picoctf 4096 Mar 12  2024 .git
-rw-r--r-- 1 JorgeAlamillo-picoctf JorgeAlamillo-picoctf   22 Mar 12  2024 message.py

JorgeAlamillo-picoctf@webshell:~/drop-in$ git blame message.py

8c83358c (picoCTF{@sk_th3_1nt3rn_2c6bf174} 2024-03-12 00:07:11 +0000 1) print("Hello, World!"
```

### Notas
- `git blame` te muestra, línea por línea, quién fue la última persona que modificó un archivo.