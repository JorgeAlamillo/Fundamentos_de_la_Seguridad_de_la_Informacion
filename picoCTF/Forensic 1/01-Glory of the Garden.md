### Glory of the Garden

### Descripción

This file contains more than it seems.Get the flag from [garden.jpg](https://challenge-files.picoctf.net/c_fickle_tempest/39ad2588c3c0db341eff579d7cf894efc34a3b8174368eee2ea0e5ea06516238/garden.jpg).
### Solución

### Solucion 

- Descargamos la imagen `garden.jpg` usando el comando wget en la terminal de Kali Linux.
```
wget -q https://challenge-files.picoctf.net/c_fickle_tempest/39ad2588c3c0db341eff579d7cf894efc34a3b8174368eee2ea0e5ea06516238/garden.jpg
```

- Navegamos a la carpeta donde se encontraba el archivo y verificamos su existencia con el comando ls.

- Ejecutamos el comando `strings garden.jpg | grep pico` para buscar la bandera directamente.
```
┌──(JorgeMSI㉿MSI)-[~]
└─$ strings garden.jpg | grep pico
```

- Obtenemos la bandera.
```
┌──(JorgeMSI㉿MSI)-[~]
└─$ strings garden.jpg | grep pico
Here is a flag: picoCTF{more_than_m33ts_the_3y339cbe6dc}

```
picoCTF{more_than_m33ts_the_3y339cbe6dc}

### Notas
- **`strings`** es una herramienta diseñada para filtrar y mostrar únicamente las secuencias de caracteres imprimibles (texto) dentro de archivos que no son de texto, como imágenes o ejecutables.