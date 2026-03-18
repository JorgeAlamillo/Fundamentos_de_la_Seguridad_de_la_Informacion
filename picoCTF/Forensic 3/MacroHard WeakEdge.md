### MacroHard WeakEdge

### Descripción

I've hidden a flag in this file. Can you find it?[Forensics_is_fun.pptm](https://challenge-files.picoctf.net/c_wily_courier/d78815176c19ddc85a1388233268d2f4c459fcbbaab197b4a29ebafc88294c54/Forensics_is_fun.pptm)
### Solución

- Se revisó el archivo con el comando file para confirmar que, aunque termina en .pptm, es en realidad un archivo comprimido (ZIP). bash file Forensics_is_fun.pptm

- Se utilizó unzip para extraer todo el contenido del paquete de Office y poder navegar por sus carpetas internas. bash unzip Forensics_is_fun.pptm

- Al explorar las carpetas, se encontró un archivo sospechoso llamado "hidden" dentro de la ruta de las diapositivas maestras. 

     cd ppt/slideMasters ls

- Limpieza y decodificación Se detectó que el archivo contenía una cadena en Base64 con espacios. Se usó tr para eliminar los espacios y base64 para traducir el código a texto legible. bash cat hidden | tr -d ' ' | base64 -d

┌──(JorgeMSI㉿MSI)-[~/MAcro/reto_forensics/ppt/slideMasters]
└─$ cat hidden | tr -d ' ' | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}
### Notas
### Referencia
