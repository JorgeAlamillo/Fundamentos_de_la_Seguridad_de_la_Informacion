###  Glitch Cat

### Descripción

Our flag printing service has started glitching!`$ nc saturn.picoctf.net 58464`
### Solución

### Solucion 1 - Usando Consola

```
nc saturn.picoctf.net 58464
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
^C

$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.

>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'

'picoCTF{gl17ch_m3_n07_bda68f75}'
```

### Notas
- nc se conecta al servidor para ver si un puerto esta activo.
- En el interprete de python puedo ejecutar cualquier sentencia del lenguaje.