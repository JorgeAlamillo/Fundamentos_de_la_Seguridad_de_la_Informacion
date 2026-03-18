### WebNet0

### Descripción

We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/picopico.key). Recover the flag.
### Solución

- Verificamos el tipo de archivo, uno es una captura de paquetes, el otro una llave rsa con la que fue encriptado el tráfico TLS en el paquete

`file capture.pcap 
`file picopico.key`

- Decodificamos el paquete usando la llave rsa con `ssldump`:
`ssldump -r capture.pcap -k picopico.key -d | grep pico -A 2`

picoCTF{nongshim.shrimp.crackers}

### Notas
### Referencias
