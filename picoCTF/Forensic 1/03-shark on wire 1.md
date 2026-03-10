### shark on wire 1

### Descripción

We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/134d2a2cf6ec5b7e757effc9b32977af7cc324b8e99a5ddb64737794a14dc18d/capture.pcap). Recover the flag.
### Solucion 

- Lanzamos la herramienta: Abrimos Wireshark desde la terminal de Kali Linux cargando directamente el archivo con el comando wireshark capture.pcap &.

- Limpiamos la vista: En la barra de Apply a display filter, escribimos udp y presionamos Enter para filtrar solo los paquetes de este protocolo.

- Interceptamos la conversación: Hicimos clic derecho sobre uno de los paquetes UDP y seleccionamos la opción Follow -> UDP Stream.

- Exploramos los flujos: En la ventana emergente, navegamos por los diferentes hilos de conversación usando el selector de Stream en la esquina inferior derecha.

- Identificamos el objetivo: Al llegar al Stream 6, el contenido cambió de caracteres aleatorios a texto legible.

- Extrajimos la bandera: Copiamos la bandera picoCTF{StaT31355_636f6e6e} que aparecía en pantalla y la pegamos en la plataforma.

### Notas 
- Wireshark nos permite ver la "conversación" completa entre dos computadoras.
- Al usar Follow UDP Stream, Wireshark junta todos los paquetes pequeños que están dispersos y nos los muestra como un solo mensaje legible, lo que facilita encontrar la bandera sin tener que revisar los miles de paquetes uno por uno.

