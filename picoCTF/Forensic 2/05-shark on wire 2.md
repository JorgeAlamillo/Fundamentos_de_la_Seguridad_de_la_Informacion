### shark on wire 2

### Descripción

Decode this [message](https://challenge-files.picoctf.net/c_fickle_tempest/d372c5aa057b687f120292b30c70af827c64bd3661490e3e2f41551ff95394f0/message.wav) from the moon.
### Solución

Instalamos la librería necesaria para que Python pueda leer archivos de red (.pcap) con el comando: `sudo apt install python3-scapy -y`

Creamos el archivo para nuestro script usando el editor de texto de la terminal: `nano exploit.py`

Copiamos y pegamos el siguiente código
```
from scapy.all import *

packets = rdpcap('capture.pcap')

flag=''

for p in packets:
    if UDP in p and p[UDP].dport == 22:
        if p[UDP].sport > 5000:
            flag+=chr(p[UDP].sport - 5000)

print(flag)
```

Ejecutamos el exploit con Python para que procese todos los paquetes y nos imprima la bandera directamente: `python3 exploit.py`

picoCTF{p1LLf3r3d_data_v1a_st3g0}
