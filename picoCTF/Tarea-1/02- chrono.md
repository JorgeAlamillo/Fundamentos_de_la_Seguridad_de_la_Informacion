### chrono

### Descripción

How to automate tasks to run at intervals on linux servers?Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 65116
Username: picoplayer 
Password: pYkku7iMsS
```
### Solución

### Solucion 1 - Usando Consola

```
ssh -p 65116 picoplayer@saturn.picoctf.net
picoplayer@saturn.picoctf.net's password:pYkku7iMsS

picoplayer@challenge:~$ crontab -l

picoplayer@challenge:~$ cd /

picoplayer@challenge:/$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_7754e199}
picoplayer@challenge:/$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed. 
```

### Notas
- `crontab -l` solo te muestra las tareas de tu usuario actual
- `/etc/crontab` Es donde el administrador programa procesos que afectan a todo el sistema o que deben ejecutarse bajo usuarios específicos (como `root`).
