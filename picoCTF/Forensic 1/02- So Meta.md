### So Meta

### Descripción

Find the flag in this [picture](https://challenge-files.picoctf.net/c_fickle_tempest/8e74516a5167183bf254f082a836fe7b925c25d6899feeffb68f78b1549a1224/pico_img.png).
### Solución

### Solucion 

- Descargamos la imagen `pico_img.png` desde el enlace del reto en nuestra terminal de Kali Linux.
```
┌──(JorgeMSI㉿MSI)-[~]
└─$ wget -q https://challenge-files.picoctf.net/c_fickle_tempest/8e74516a5167183bf254f082a836fe7b925c25d6899feeffb68f78b1549a1224/pico_img.png
```
- Usamos el comando `exiftool pico_img.png` para leer todos los metadatos incrustados en la imagen.
```
┌──(JorgeMSI㉿MSI)-[~]
└─$ exiftool pico_img.png
```

- Revisamos 
Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
Artist                          : picoCTF{s0_m3ta_9a8b5aa1}
Image Size                      : 600x600
Megapixels                      : 0.360

Vemos que en Artist esta la bandera incrustada.

- picoCTF{s0_m3ta_9a8b5aa1}

### Notas
- **`exiftool`** es la herramienta estándar para leer, escribir y editar información de metadatos en una enorme variedad de archivos