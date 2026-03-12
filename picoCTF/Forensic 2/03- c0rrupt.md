### c0rrupt

### Descripción

We found this [file](https://challenge-files.picoctf.net/c_fickle_tempest/87bdc8ce30b177d033b3d68bca4647950bb07304032861baa912ebe08701d355/mystery). Recover the flag.
### Solución
Descargamos el archivo mystery usando el comando wget para guardarlo en nuestra carpeta de trabajo en Kali Linux.

Ejecutamos el comando file mystery y confirmamos que el sistema lo identifica como data, lo que significa que el encabezado está roto y no se reconoce como imagen.

Abrimos el archivo para edición técnica con el comando hexeditor mystery.

Reparamos la firma del archivo escribiendo directamente sobre los primeros 8 bytes para que queden como 89 50 4E 47 0D 0A 1A 0A. Esto le dice al sistema que el archivo es un PNG.

Buscamos la cadena corrupta 43 22 44 52 y escribimos encima 49 48 44 52 para restaurar el bloque IHDR, que contiene la información de tamaño y profundidad de la imagen.

Guardamos los cambios con Ctrl+O, salimos con Ctrl+X e instalamos la herramienta de diagnóstico con el comando sudo apt install pngcheck.

Ejecutamos el comando pngcheck -v mystery para encontrar el siguiente error, el cual nos indicó que el bloque pHys era inválido.

Entramos de nuevo con hexeditor mystery, buscamos la secuencia aa 00 16 25 00 00 16 25 y la corregimos escribiendo 00 00 16 25 00 00 16 25.

Corremos otra vez el comando pngcheck -v mystery para detectar errores en el tamaño de los bloques de datos.

Localizamos los bytes AA AA FF A5 en el editor hexadecimal y los reemplazamos por 00 00 FF A5 para corregir el valor de longitud del chunk.

Buscamos justo después la etiqueta corrupta AB 44 45 54 y escribimos encima 49 44 41 54 para que el bloque sea reconocido como IDAT (donde están los píxeles reales).

Guardamos con Ctrl+O y salimos con Ctrl+X por última vez.

Verificamos que el archivo ya es válido con el comando file mystery, que ahora nos debe mostrar que es una imagen PNG correcta.

Abrimos el archivo con el comando eog mystery para visualizar la imagen recuperada y leer la bandera.

picoCTF{c0rrupt10n_1847995}