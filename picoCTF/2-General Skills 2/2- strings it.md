### strings it

### Descripción

Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/53c039e64942b1c4334781c4987ba7e2ba54f0b2bf39f52c65f3a65dfcbf4194/strings) without running it?
### Solución

### Solucion 1 - Usando Consola

```
wget https://challenge-files.picoctf.net/c_fickle_tempest/53c039e64942b1c4334781c4987ba7e2ba54f0b2bf39f52c65f3a65dfcbf4194/strings

strings strings | grep "picoCTF"

picoCTF{5tRIng5_1T_A1b9ECAa}

```

### Notas
- strings extrae texto de archivos binarios.
