### Big Zip

### Descripción

Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)
### Solución

### Solución 1 - Usando Consola

```
 wget https://artifacts.picoctf.net/c/503/big-zip-files.zip
 
 unzip big-zip-files.zip 
 
grep -r "picoCTF" big-zip-files/                     
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode 

picoCTF{gr3p_15_m4g1c_ef8790dc}
```

### Notas
- -r hace que entre en cada subcarpeta de la carpeta principal y busque lo señalado. 