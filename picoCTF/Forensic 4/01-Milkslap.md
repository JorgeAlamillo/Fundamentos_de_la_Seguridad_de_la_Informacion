### Milkslap

🥛http://wily-courier.picoctf.net:55605/

### Solución

1. Inspeccionamos el sitio web y notamos que la animación de la bofetada depende de una interacción con el ratón.
    
2. Analizamos el código fuente con curl o el inspector del navegador para localizar el recurso principal.
    
3. Identificamos y descargamos el archivo único de la página: una imagen PNG llamada concat_v.png.
    
4. Seleccionamos la herramienta zsteg (especializada en PNG) tras descartar steghide (solo para JPG).
    
5. Ejecutamos zsteg concat_v.png para inspeccionar los bits menos significativos (LSB) de los canales de color.
    
6. Extraemos la bandera que aparece en la salida de la terminal, ignorando el salto de línea (\n).
    

picoCTF{imag3_m4n1pul4t10n_sl4p5}
### Notas

### Referencias
