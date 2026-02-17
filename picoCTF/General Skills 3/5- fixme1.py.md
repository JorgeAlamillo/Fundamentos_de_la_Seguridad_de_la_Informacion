### fixme1.py

### Descripción

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
### Solución

### Solucion 1 - Usando Consola

```
wget -q https://artifacts.picoctf.net/c/25/fixme1.py

nano fixme1.py

"Se modifica y se hace que el print este al mismo nivel que flag  "
"flag = str_xor(flag_enc, 'enkidu')
 print('That is correct! Here\'s your flag: ' + flag)"

python fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```

