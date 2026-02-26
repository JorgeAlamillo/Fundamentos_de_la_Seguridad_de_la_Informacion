### Scavenger Hunt

### Descripción

There is some interesting information hidden around this site. Can you find it?[http://wily-courier.picoctf.net:64257/](http://wily-courier.picoctf.net:64999/)

### Solución

### Solucion 1 visualizando código fuente

```
Abrimos codigo fuente y abajo sale la primera parte de la bandera 

picoCTF{t

Abrimos mycss.css y hasta abajo sale la segunda parte de la bandera 

h4ts_4_l0

Abrimos myjs.js y hasta abajo dice: ¿Cómo puedo impedir que Google indexe mi página web?, y nosotros que robots.txt es para esto. entonces ponermos el siguiente url 
http://wily-courier.picoctf.net:64257/robots.txt
y viene la tercera parte de la flag 

t_0f_pl4c

Y abajo dice: 

"Creo que este es un servidor Apache... ¿puedes acceder a la siguiente bandera?"

Ponemos el siguiente link:
http://wily-courier.picoctf.net:64999/.htaccess

y obtenemos la siguiente parte de la bandera:

3s_2_lO0k

Abajo dice lo siguiente:

"Me encanta crear sitios web en mi Mac, puedo almacenar mucha información allí".

Ponemos el siguiente link para la ultima parte de la bandera:

http://wily-courier.picoctf.net:64999/.DS_Store

y la ultima parte de la bandera es:

_9588550}

Juntando todas las banderas el resultado es:

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_9588550}



```


### Notas
- htaccess: proporciona una forma de hacer cambios a la configuración en el contexto de un directorio.
- .DS_Store es un archivo generado por macOS que almacena atributos personalizados de la carpeta que lo contiene, tales como las opciones de vista, las posiciones de los iconos y otra información visual. El nombre es una abreviatura de Desktop Services Store (Almacén de Servicios de Escritorio).
### Referencias
- https://www.youtube.com/watch?v=LseQ-XWCXVo&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=13
- https://en.wikipedia.org/wiki/.DS_Store