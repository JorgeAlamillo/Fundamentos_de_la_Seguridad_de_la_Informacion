### Special

### Descripción

Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.`ssh -p 64078 ctf-player@saturn.picoctf.net`The password is `fd7746b4`
### Solución

### Solucion 1 - Usando Consola

```
ssh -p 64078 ctf-player@saturn.picoctf.net
ctf-player@saturn.picoctf.net's password: fd7746b4

Special$ Clear & find. 
Clear & find 
sh: 1: Clear: not found
.
./blargh
./blargh/flag.txt
./.cache
./.cache/motd.legal-displayed
Special$ Clear & cat ./blargh/flag.txt
Clear & cat ./blargh/flag.txt 
sh: 1: Clear: not found
picoCTF{5p311ch3ck_15_7h3_w0r57_f578af59}
```

### Notas 
- En Linux, el `&` separa comandos. Al ponerlo, le dijo al sistema: "Ejecuta lo que está a la izquierda y, al mismo tiempo o inmediatamente después, ejecuta lo de la derecha".
- Al escribir `Clear`, el shell se enfocó en esa palabra, intentó procesarla y falló. Pero lo importante es que gastó su "energía" de corrección en esa primera palabra.
- El comando `find` por sí solo busca archivos, pero el punto `.` le indica al sistema: busca en la carpeta donde estoy parado ahora mismo.