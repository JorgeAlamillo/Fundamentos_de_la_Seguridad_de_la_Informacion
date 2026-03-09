### Local Authority

### Descripción

Can you get the flag?Go to this [website](http://saturn.picoctf.net:53291/) and see what you can discover.
### Solución

### Solucion 

Primero abrimos la pagina web. Asignamos un usuario y un password aleatorio.

Abrimos el código fuente después de que nos dijo que tenemos mal el usuario y la contraseña.

Abrimos el secure.jss <script src="[secure.js](http://saturn.picoctf.net:53291/secure.js)"></script>

Tiene el siguiente Codigo
```
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```

Vemos que el usuario es admin y la contraseña strongPassword098765

Regresamos y ponemos el usuario y contraseña correcta.

Y obtenemos la bandera.
picoCTF{j5_15_7r4n5p4r3n7_05df90c8}
