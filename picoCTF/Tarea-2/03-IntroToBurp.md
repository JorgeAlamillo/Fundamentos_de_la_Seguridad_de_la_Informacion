### IntroToBurp

### Descripción

Try [here](http://titan.picoctf.net:59517/) to find the flag
### Solución

### Solucion 1

Primero, abrimos Burp Suite desde la terminal de Kali Linux en WSL. Como estamos trabajando en un entorno híbrido, decidimos usar el botón Open Browser dentro de la pestaña Proxy para no tener que lidiar con configuraciones manuales de red en Windows. Una vez abierto el navegador de Burp, entramos a la URL del reto de picoCTF.

Activamos el botón Intercept is ON en Burp Suite para que actuara como un muro entre mi navegador y el servidor. En la página de registro, llenamos los campos con cualquier dato (yo usé datos genéricos como "Jorge") y le dimos a Register. En Burp, vimos aparecer la petición `POST /`. Simplemente le dimos a Forward para dejarla pasar, ya que lo que nos interesaba era el siguiente paso: la validación.

Cuando el navegador nos pidió el código OTP, escribimos cualquier número (por ejemplo, 123) y le dimos a enviar. Rápidamente regresamos a Burp, donde la petición se quedó congelada. Identificamos al final del texto la línea que decía `otp=123`.

Aquí es donde hicimos el truco: borramos completamente esa parte. No dejamos rastro de la palabra otp ni del signo igual. Dejamos ese espacio vacío y le dimos clic a Forward.

Al enviarle al servidor una petición "incompleta", provocamos un error en su lógica de validación. En lugar de rechazarnos, el servidor se confundió y nos dejó entrar directamente al Dashboard. 

picoCTF{#0TP_Bypvss_SuCc3$S_6bffad21}

