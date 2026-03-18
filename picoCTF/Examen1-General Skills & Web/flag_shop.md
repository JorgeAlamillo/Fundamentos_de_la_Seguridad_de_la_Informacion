### flag_shop

### Descripcion

There's a flag shop selling stuff, can you buy a flag?[Source](https://challenge-files.picoctf.net/c_fickle_tempest/66a0d80bfdedc5f74bdd52c50da2e5d7bf40c5634fd456b103ac74c006bf45e4/store.c). Connect with nc fickle-tempest.picoctf.net 62821.

### Solucion

Primero, nos conectamos al servidor abriendo nuestra terminal y tecleando nc fickle-tempest.picoctf.net 62821.

Una vez adentro, el menú nos mostrará nuestras opciones y nuestro balance actual, que normalmente es de unos mil dólares, pero la bandera real cuesta cien mil. Para hacernos millonarios, elegimos la opción para comprar banderas, y luego seleccionamos comprar las banderas de imitación.

Cuando el sistema nos pregunte cuántas banderas de imitación queremos comprar, aquí es donde hacemos la trampa. En lugar de pedir una o dos, escribimos un número grandísimo, por ejemplo 3000000 y presionamos Enter.

Al hacer la multiplicación del costo por esa cantidad tan gigante, el resultado supera el límite de memoria que el programa puede calcular y se rompe, convirtiéndose en un número negativo. Como el sistema nos resta ese costo de nuestra cuenta, al restar un número negativo, matemáticamente nos lo termina sumando.

De pronto veremos que nuestro balance ahora es de millones de dólares. Ya con ese dinero de sobra en la cuenta, simplemente volvemos al menú de compras, elegimos la opción para comprar la bandera real de 100000 dólares y el servidor nos entregará nuestra bandera directamente en la 

pantalla.picoCTF{m0n3y_bag5_39AF2bE1}

### Notas

### Referencias