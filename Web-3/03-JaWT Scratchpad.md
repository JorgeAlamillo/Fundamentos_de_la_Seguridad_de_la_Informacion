### JaWT Scratchpad

### Descripción

Check the admin scratchpad!http://fickle-tempest.picoctf.net:49860
### Solución

### Solucion 1

- Entramos a la app y nos logeamos como John.
- Vamos al cookie editor y copiamos la cookie que nos genero
- nos vamos a jwt debugger y ponemos la cookie copiada
- modificamos el nombre y le cambiamos a admin
- copiamos la cookie y la ponemos en terminal usando el comando john eltokenchido -w=/usr/share/wordlists/rockyou.txt
- eltokenchido tiene dentro la cookie generada
- cambiamos por ilovepico en el jwt debugger
- copiamos la cookie y la pegamos en la pagina, guardamos y reiniciamos

picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}

### Referencias
- JSON: [https://en.wikipedia.org/wiki/JSON](https://en.wikipedia.org/wiki/JSON "https://en.wikipedia.org/wiki/JSON")
- JWT : [https://jwt.io/introduction](https://jwt.io/introduction "https://jwt.io/introduction")
- jwt debugger : [https://jwt.lannysport.net/](https://jwt.lannysport.net/ "https://jwt.lannysport.net/")
- john : [https://github.com/openwall/john](https://github.com/openwall/john "https://github.com/openwall/john")
