### Time Machine

### Descripción

What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/68/challenge.zip)
### Solución

### Solucion 1 - Usando Consola

```
wget -q https://artifacts.picoctf.net/c_titan/68/challenge.zip
JorgeAlamillo-picoctf@webshell:~$ unzip challenge.zip 

JorgeAlamillo-picoctf@webshell:~$ ls                     
README.txt  challenge.zip  drop-in  home
JorgeAlamillo-picoctf@webshell:~$ cd drop-in/
JorgeAlamillo-picoctf@webshell:~/drop-in$ ls
message.txt
JorgeAlamillo-picoctf@webshell:~/drop-in$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...

JorgeAlamillo-picoctf@webshell:~/drop-in$ ls -la
total 12
drwxr-xr-x 3 JorgeAlamillo-picoctf JorgeAlamillo-picoctf   49 Mar  9  2024 .
drwxr-xr-x 7 JorgeAlamillo-picoctf JorgeAlamillo-picoctf 4096 Feb 21 02:50 ..
drwxr-xr-x 8 JorgeAlamillo-picoctf JorgeAlamillo-picoctf 4096 Mar  9  2024 .git
-rw-r--r-- 1 JorgeAlamillo-picoctf JorgeAlamillo-picoctf   87 Mar  9  2024 message.txt
JorgeAlamillo-picoctf@webshell:~/drop-in$ git log

picoCTF{t1m3m@ch1n3_b476ca06}
```

