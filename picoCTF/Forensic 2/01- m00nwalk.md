### m00nwalk

### Descripción

Decode this [message](https://challenge-files.picoctf.net/c_fickle_tempest/d372c5aa057b687f120292b30c70af827c64bd3661490e3e2f41551ff95394f0/message.wav) from the moon.
### Solución

- Descargamos el archivo message.wav directamente a nuestra carpeta de trabajo en Kali Linux usando el comando wget -q [https://challenge-files.picoctf.net/c_fickle_tempest/d372c5aa057b687f120292b30c70af827c64bd3661490e3e2f41551ff95394f0/message.wav](https://challenge-files.picoctf.net/c_fickle_tempest/d372c5aa057b687f120292b30c70af827c64bd3661490e3e2f41551ff95394f0/message.wav).

- Instalamos las librerías de soporte y el paquete de herramientas con el comando sudo apt install python3-setuptools libfftw3-dev libpulse-dev -y para que el sistema pudiera procesar el decodificador.

- Clonamos el repositorio del decodificador desde GitHub usando el comando git clone [https://github.com/colaclanth/sstv.git](https://www.google.com/search?q=https://github.com/colaclanth/sstv.git) y entramos a la carpeta con cd sstv.

- Ejecutamos la instalación de la herramienta con el comando sudo python3 setup.py install para registrar el programa en nuestro sistema.

- Regresamos a nuestra carpeta principal con cd .. y corrimos el comando sstv -d message.wav -o resultado.png para transformar los sonidos del audio en una imagen.

- Abrimos el archivo generado usando el comando eog resultado.png para visualizar la bandera que estaba oculta en las frecuencias de radio.

- picoCTF{beep_boop_im_in_space}