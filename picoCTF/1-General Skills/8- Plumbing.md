###  plumbing

### Descripción

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?Connect to fickle-tempest.picoctf.net 57178.
### Solución

### Solucion 1 - Usando Consola

```
nc fickle-tempest.picoctf.net 57178 | grep pico

picoCTF{digital_plumb3r_00da27CC}

```

### Notas
- nc se conecta al servidor para ver si un puerto esta activo.
- | redirige la salida de un comando a la entrada de otro.
- > redirige la salida de un comando a un archivo de texto.
