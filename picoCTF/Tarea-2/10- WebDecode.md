### WebDecode

### Descripción

Do you know how to use the web inspector?Start searching [here](http://titan.picoctf.net:58294/) to find the flag
### Solución

- Entramos a la URL del reto y navegamos por las pestañas del sitio (Home, About, Contact).
- Abrimos el Inspector y seleccionamos la pestaña Elements.
- En la sección "About", localizamos una cadena de texto codificada en un atributo de una etiqueta HTML.
- Copiamos esa cadena de texto que terminaba en == cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMWY4MzI2MTV9.
- Fuimos a la terminal de Kali Linux (WSL) y ejecutamos el comando: `echo "cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMWY4MzI2MTV9==" | base64 -d`.
- Obtuvimos la bandera directamente en la terminal y la pegamos en picoCTF.
- picoCTF{web_succ3ssfully_d3c0ded_1f832615}

Encontramos la bandera 

picoCTF{web_succ3ssfully_d3c0ded_1f832615}
