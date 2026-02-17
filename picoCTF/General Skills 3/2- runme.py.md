### Super SSH

### Descripción

Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
### Solución

### Solucion 1 - Usando Consola

```
wget -q https://artifacts.picoctf.net/c/34/runme.py

cat runme.py 
#!/usr/bin/python3
################################################################################
# Python script which just prints the flag
################################################################################

flag ='picoCTF{run_s4n1ty_run}'
print(flag)
```

