### First Grep

### Descripción
Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way.The flag is in this [file](https://challenge-files.picoctf.net/c_fickle_tempest/2e9bfa4e1d90ac25a999fefdfb4feb8a2ff4eb73e4c61af4889a3762687ada01/file).
### Solución

### Solucion 1 - Usando Consola

```
wget https://challenge-files.picoctf.net/c_fickle_tempest/2e9bfa4e1d90ac25a999fefdfb4feb8a2ff4eb73e4c61af4889a3762687ada01/file

grrp "picoCTF" file

picoCTF{grep_is_good_to_find_things_29f42460}
```

### Notas
- wget permite descargar archivos desde la consola y para usarlos ahí.
- grep encuentra una cadena en un archivo de texto.
### Referencias
- https://gchq.github.io/CyberChef
