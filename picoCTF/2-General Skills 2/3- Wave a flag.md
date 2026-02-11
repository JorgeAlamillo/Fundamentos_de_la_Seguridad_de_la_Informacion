### Wave a flag

### Descripción

Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...[warm](https://challenge-files.picoctf.net/c_wily_courier/5a478d0b24d6a4f4185e3adb7a78c41cdad626fb02fe80e083dc33bf8b197d3d/warm)
### Solución

### Solucion 1 - Usando Consola

```
wget https://challenge-files.picoctf.net/c_wily_courier/5a478d0b24d6a4f4185e3adb7a78c41cdad626fb02fe80e083dc33bf8b197d3d/warm
--2026-02-10 20:52:15--  https://challenge-files.picoctf.net/c_wily_courier/5a478d0b24d6a4f4185e3adb7a78c41cdad626fb02fe80e083dc33bf8b197d3d/warm
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.18, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19312 (19K) [application/octet-stream]
Saving to: 'warm'

warm                  100%[=======================>]  18.86K  --.-KB/s    in 0.006s  

2026-02-10 20:52:15 (3.22 MB/s) - 'warm' saved [19312/19312]

JorgeAlamillo-picoctf@webshell:~$ -h
-bash: -h: command not found
JorgeAlamillo-picoctf@webshell:~$ chmod +x warm
JorgeAlamillo-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
```

### Notas
- -h ayuda para saber que otras opciones tiene disponibles
- chmod +x da permisos para poder ser ejecutado un archivo.


