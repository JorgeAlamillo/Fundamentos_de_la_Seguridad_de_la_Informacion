### What Lies Within

### Descripción

There's something in the [building](https://challenge-files.picoctf.net/c_fickle_tempest/c0eec6af0f04316e2bdc4a9f095afd0e2d0121f5e543dbc4a65bb0038d72a993/buildings.png). Can you retrieve the flag?
### Solución

- Entramos a una página de esteganografía como StegOnline o Stylesu.

- Subimos el archivo buildings.png a la plataforma.

- Buscamos la opción llamada Extract Files o Browse Bit Planes.

- Seleccionamos los canales de color Rojo, Verde y Azul (RGB) en el bit 0, que es donde se suele esconder la información en estos retos.

- Revisamos el texto extraído hasta encontrar la bandera

- picoCTF{h1d1ng_1n_th3_b1t5}


### Notas

- La esteganografía es la técnica de ocultar mensajes o información secreta dentro de otro objeto que parece inofensivo, como una imagen, un audio o un video, de manera que nadie sospeche que hay algo escondido.
### Referencias
- https://georgeom.net/StegOnline/extract