### Collaborative Development

### Descripción

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/70/challenge.zip)
### Solución

### Solucion 1 - Usando Consola

```
JorgeAlamillo-picoctf@webshell:~$ wget -q https://artifacts.picoctf.net/c_titan/70/challenge.zip
JorgeAlamillo-picoctf@webshell:~$ unzip challenge.zip 

JorgeAlamillo-picoctf@webshell:~$ ls
challenge.zip  drop-in
JorgeAlamillo-picoctf@webshell:~$ cd drop-in/
JorgeAlamillo-picoctf@webshell:~/drop-in$ ls
flag.py
JorgeAlamillo-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")
JorgeAlamillo-picoctf@webshell:~/drop-in$ ls -la
total 12
drwxr-xr-x 3 JorgeAlamillo-picoctf JorgeAlamillo-picoctf   45 Mar  9  2024 .
drwxr-xr-x 6 JorgeAlamillo-picoctf JorgeAlamillo-picoctf 4096 Feb 21 03:01 ..
drwxr-xr-x 8 JorgeAlamillo-picoctf JorgeAlamillo-picoctf 4096 Mar  9  2024 .git
-rw-r--r-- 1 JorgeAlamillo-picoctf JorgeAlamillo-picoctf   30 Mar  9  2024 flag.py

JorgeAlamillo-picoctf@webshell:~/drop-in$ git branch -a
JorgeAlamillo-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
JorgeAlamillo-picoctf@webshell:~/drop-in$ ls
flag.py
JorgeAlamillo-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("picoCTF{t3@mw0rk_", end='')

JorgeAlamillo-picoctf@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
JorgeAlamillo-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')


JorgeAlamillo-picoctf@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
JorgeAlamillo-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("w0rk_7ffa0077}")

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ffa0077}

```

### Notas
- `git branch -a` Es para ver todas las versiones alternativas del proyecto.
- `git checkout` sirve para moverte entre diferentes versiones del proyecto.