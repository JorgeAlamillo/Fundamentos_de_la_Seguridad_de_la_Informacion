### WhitePages

### Descripción

I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.picoctf.net/c_fickle_tempest/3ba37d6bee0d96d5e3783ba94da753407f9168b61d796797f0816db5aaa86136/whitepages.txt) is all blank!
### Solución

Descargamos el archivo whitepages.txt para guardarlo en nuestra carpeta de trabajo usando el comando wget -q [https://artifacts.picoctf.net/c/59/whitepages.txt](https://www.google.com/search?q=https://artifacts.picoctf.net/c/59/whitepages.txt).

Verificamos que el archivo fuera UTF-8 con líneas muy largas usando el comando file whitepages.txt para confirmar que contenía datos invisibles.

Visualizamos el hexdump del archivo para identificar los patrones repetitivos con el comando xxd -g 1 -l 100 whitepages.txt, donde vimos las secuencias e2 80 83 y 20.

Convertimos los espacios anchos en ceros y los espacios normales en unos, y mandamos esos bits directamente a un procesador de Python con el comando: sed 's/\xe2\x80\x83/0/g' whitepages.txt | sed 's/\x20/1/g' | python3 -c "import sys; b=sys.stdin.read(); print(''.join(chr(int(b[i:i+8], 2)) for i in range(0, len(b), 8)))"

Interpretamos los bloques de 8 bits como caracteres de texto real gracias a la función del script que ejecutamos en la terminal.

SEE PUBLIC RECORDS & BACKGROUND REPORT
5000 Forbes Ave, Pittsburgh, PA 15213
picoCTF{not_all_spaces_are_created_equal_f62118c302bc9c9791e81915c805af3d}


