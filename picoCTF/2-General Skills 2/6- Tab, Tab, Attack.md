### Tab, Tab, Attack

### Descripción

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.[Addadshashanammu.zip](https://challenge-files.picoctf.net/c_wily_courier/ce53ef9432bf367be41e465224d721c1187c39debcd758efcd28e99a6b7ff7a4/Addadshashanammu.zip)

### Solución

### Solucion 1 - Usando Consola

```
wget https://challenge-files.picoctf.net/c_wily_courier/ce53ef9432bf367be41e465224d721c1187c39debcd758efcd28e99a6b7ff7a4/Addadshashanammu.zip

unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip

replace Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.c? [y]es, [n]o, [A]ll, [N]one, [r]ename: y
 
 extracting: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.c  

replace Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet? [y]es, [n]o, [A]ll, [N]one, [r]ename: y
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Ma
elkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet

cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/

JorgeAlamillo-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls

fang-of-haynekhtnamet  fang-of-haynekhtnamet.c

JorgeAlamillo-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ grep "pico" fang-of-haynekhtnamet

grep: fang-of-haynekhtnamet: binary file matches

JorgeAlamillo-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ 

JorgeAlamillo-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$

 strings fang-of-haynekhtnamet | grep "pico"       

*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}

```

### Notas
- El teclear Tab ayuda demasiado en palabras largas, a la velocidad y a la precisión en terminal.

