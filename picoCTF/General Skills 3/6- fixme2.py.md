### fixme2.py

### Descripción

Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)
### Solución

### Solucion 1 - Usando Consola

```
wget -q https://artifacts.picoctf.net/c/6/fixme2.py

JorgeAlamillo-picoctf@webshell:~$ nano fixme2.py 

"modificar y ponerle == al if" 
"if flag =  "":
  print('String XOR encountered a problem, quitting.')"

JorgeAlamillo-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```

