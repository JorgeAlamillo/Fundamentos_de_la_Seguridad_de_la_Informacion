### Static ain't always noise

### Descripción

Can you look at the data in this binary? The bash script might help [static](https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/static), [ltdis.sh](https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/ltdis.sh)
### Solución

### Solucion 1 - Usando Consola

```
wget https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/static

wget https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/ltdis.sh

chmod +x ltdis.sh

./ltdis.sh static

Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset

grep "pico" static.ltdis.strings.txt

3020 picoCTF{d15a5m_t34s3r_20335e41}
```

### Notas
- chmod +x da permisos para poder ser ejecutado un archivo.




