### WebNet1

### Descripción

We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/picopico.key). Recover the flag.
### Solución

Abrimos el archivo con Wireshark

`wireshark capture.pcap &` 

Cambiar la llave rsa , Ve a Edit - Preferences - Protocols - TLS , copiamos la llave descargada

Extraer la imagen en el trafico

- Vamos a File - Export Objects - HTTP
- Selecciona el archivo `vultre.jpg` que es el 91

- Click en Save
- Extrae las cadenas en la imagen con el siguiente comando
`strings -n 10 vulture.jpg`

┌──(JorgeMSI㉿MSI)-[~/webnet1]
└─$ strings -n 10 vulture.jpg
picoCTF{honey.roasted.peanuts}
ICC_PROFILE
mntrRGB XYZ
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
%'c^;XRs(A
-%0c;I?Q^Gq~
_jDrp3\576
;PFM/cY5wp
z8i9J+}Gf|


picoCTF{honey.roasted.peanuts}
### Notas
### Referencias
