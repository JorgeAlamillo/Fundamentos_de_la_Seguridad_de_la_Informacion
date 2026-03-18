### tunn3l v1s10n

### Descripción

We found this file. Recover the flag.[tunn3l_v1s10n](https://challenge-files.picoctf.net/c_wily_courier/626df9feed926c1e1280804f5d87fde5576e266ff250a819a5528b0471b0f3f7/tunn3l_v1s10n)
### Solución

- Con hexeditor, tenemos que modificar los offset del archivo, para obtener una imagen mas grande.


En el offset 0xE, verificamos
`xxd -s 0xc -l 4 tunn3l_v1s10n 0000000c: 0000 bad0   xxd -s 0xc -l 4 tunn3l_v1s10n 0000000c: 0000 2800`

En el offset 0xA, verificamos
`xxd -s 0x8 -l 4 tunn3l_v1s10n 00000009: 0000 bad0     xxd -s 0x8 -l 4 tunn3l_v1s10n 00000008: 0000 2800`


Modificamos la altura en el offset 0x16 y le ponemos la misma altura que aparece en el offset 0x12 para hacer la imagen simétrica, y verificamos
`xxd -s 0x14 -l 4 tunn3l_v1s10n 00000014: 0000 3201       xxd -s 0x14 -l 4 tunn3l_v1s10n 00000014: 0000 6e04`


picoCTF{qu1t3_a_v13w_2020}

### Notas
### Referencia
