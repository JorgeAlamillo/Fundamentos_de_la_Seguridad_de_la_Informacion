### where are the robots

### Descripción

Can you find the robots? http://fickle-tempest.picoctf.net:59518
### Solución

### Solucion 1 

```
Entramos al documento de texto robots.txt para ver informacion adicional sobre el sitio web.
 
http://fickle-tempest.picoctf.net:59518/robots.txt

Ahi nos da esto:
User-agent: *
Disallow: /cc6b1.html

que usaremos para entrar a el siguiente url:
http://fickle-tempest.picoctf.net:59518/cc6b1.html

picoCTF{ca1cu1at1ng_Mach1n3s_cc6b1}
```

### Notas
- Un archivo **`robots.txt`** es un documento de texto simple que se coloca en el directorio raíz de un sitio web para dar instrucciones a los rastreadores de los motores de búsqueda (conocidos como _bots_ o _spiders_, como Googlebot).
### Referencias
- Gemini IA