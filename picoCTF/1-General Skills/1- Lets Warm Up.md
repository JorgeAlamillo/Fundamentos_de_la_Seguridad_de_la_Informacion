### Lets Warm Up

### Descripción
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

### Solución

### Solucion 1 - Usando cyberchef
https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg3MA

p

picoCTF{p}
### Solucion 2 - Usando Python

```
python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> int(0x70)
112
>>> chr(112)
'p'
```
### Notas
- Cyberchef es una pagina que me permite decodificar en diferentes formatos
### Referencias
- https://gchq.github.io/CyberChef
