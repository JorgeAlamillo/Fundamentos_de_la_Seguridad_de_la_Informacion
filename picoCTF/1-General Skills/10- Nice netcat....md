###  Nice netcat...

### Descripción

There is a nice program that you can talk to by using this command in a shell:$ nc wily-courier.picoctf.net 56861, but it doesn't speak English...
### Solución

### Solucion 1 - Usando Consola

```
nc wily-courier.picoctf.net 56861
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
100 
57 
52 
55 
54 
125 
10 
```
- https://gchq.github.io/CyberChef/#recipe=From_Decimal('Space',false)&input=MTEyIAoxMDUgCjk5IAoxMTEgCjY3IAo4NCAKNzAgCjEyMyAKMTAzIAo0OCAKNDggCjEwMCAKOTUgCjEwNyAKNDkgCjExNiAKMTE2IAoxMjEgCjMzIAo5NSAKMTEwIAo0OSAKOTkgCjUxIAo5NSAKMTA3IAo0OSAKMTE2IAoxMTYgCjEyMSAKMzMgCjk1IAoxMDAgCjU3IAo1MiAKNTUgCjU0IAoxMjUgCjEwIA

### Notas
- nc se conecta al servidor para ver si un puerto esta activo.
- En el interprete de python puedo ejecutar cualquier sentencia del lenguaje.