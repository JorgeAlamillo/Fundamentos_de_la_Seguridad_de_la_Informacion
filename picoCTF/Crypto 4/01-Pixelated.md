### Pixelated

### Descripción

I have these 2 images, can you make a flag out of them?[scrambled1.png](https://challenge-files.picoctf.net/c_wily_courier/fd911d04c960ddc4effdf884e8cc954b91e1936eb4c1bdee81a39f7b16a5e465/scrambled1.png) [scrambled2.png](https://challenge-files.picoctf.net/c_wily_courier/fd911d04c960ddc4effdf884e8cc954b91e1936eb4c1bdee81a39f7b16a5e465/scrambled2.png)
### Solución

┌──(JorgeMSI㉿MSI)-[~/picoCTF/Crypto4/pixelated]
└─$ cd /opt

┌──(JorgeMSI㉿MSI)-[/opt]
└─$ sudo wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar

┌──(JorgeMSI㉿MSI)-[/opt]
└─$ sudo wget https://challenge-files.picoctf.net/c_wily_courier/fd911d04c960ddc4effdf884e8cc954b91e1936eb4c1bdee81a39f7
b16a5e465/scrambled1.png

┌──(JorgeMSI㉿MSI)-[/opt]
└─$ sudo wget https://challenge-files.picoctf.net/c_wily_courier/fd911d04c960ddc4effdf884e8cc954b91e1936eb4c1bdee81a39f7b16a5e465/scrambled2.png

┌──(JorgeMSI㉿MSI)-[/opt]
└─$ sudo chmod +x stegsolve.jar

┌──(JorgeMSI㉿MSI)-[/opt]
└─$ java -jar /opt/stegsolve.jar

Abrimos la primera imagen, la combinamos con la segunda y le movemos a ADD para obtener la flag

picoCTF{8cdf93c3}
### Notas
### Referencias