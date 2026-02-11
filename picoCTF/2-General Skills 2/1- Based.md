### Based

### Descripción

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?Connect with nc fickle-tempest.picoctf.net 64734.
### Solución

### Solucion 1 - Usando Consola y Cyberchef

```
 nc fickle-tempest.picoctf.net 64734
Let us see how data is stored
map
Please give the 01101101 01100001 01110000 as a word.
...
you have 45 seconds.....

Input:
map
Please give me the  o146 o141 o154 o143 o157 o156 as a word.
Input:
falcon
Please give me the 636f6d7075746572 as a word.
Input:
computer
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_DF19A0E8}
```

Computer hexa
https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=NjM2ZjZkNzA3NTc0NjU3Mg

map binario
https://gchq.github.io/CyberChef/#recipe=From_Binary('Space',8)&input=MDExMDExMDEgMDExMDAwMDEgMDExMTAwMDAK

falcon octal:
https://gchq.github.io/CyberChef/#recipe=From_Octal('Space')&input=MTQ2IDE0MSAxNTQgMTQzIDE1NyAxNTYK
### Notas
- nc se conecta al servidor para ver si un puerto esta activo.

### Referencias
- https://gchq.github.io/CyberChef/