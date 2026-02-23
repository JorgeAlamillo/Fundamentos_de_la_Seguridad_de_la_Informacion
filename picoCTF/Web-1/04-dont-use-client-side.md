### dont-use-client-side

### Descripción

Can you break into this super secure portal? http://fickle-tempest.picoctf.net:57893
### Solución

### Solucion 1 usando Código Fuente

```
Obtenemos el codigo fuente. Los multiplicadores de la variable `split` (como `split*2`, `split*3`, etc.) nos indican la posición exacta de cada bloque en la cadena original. Para descubrir la flag, solo tenemos que ordenar los bloques numéricamente de menor a mayor:

|if (checkpass.substring(0, split) == 'pico') {|
|if (checkpass.substring(split*6, split*7) == 'eb02') {|
|if (checkpass.substring(split, split*2) == 'CTF{') {|
|if (checkpass.substring(split*4, split*5) == 'ts_p') {|
|if (checkpass.substring(split*3, split*4) == 'lien') {|
|if (checkpass.substring(split*5, split*6) == 'lz_2') {|
|if (checkpass.substring(split*2, split*3) == 'no_c') {|
|if (checkpass.substring(split*7, split*8) == 'b45}') {|
|alert("Password Verified")|



picoCTF{no_clients_plz_2eb02b45}

```

### Notas
- **Lado del cliente** (_Client-side_) significa que el procesamiento se lleva a cabo en la computadora del usuario. Requiere que los navegadores ejecuten los scripts en la máquina del cliente sin involucrar ningún procesamiento en el servidor.
- **Lado del servidor** (_Server-side_) significa que el procesamiento tiene lugar en un servidor web.
### Referencias
- http://educative.io/answers/client-side-vs-server-side
