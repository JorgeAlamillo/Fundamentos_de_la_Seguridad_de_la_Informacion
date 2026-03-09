### Secrets

### Descripción

We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:57831/).

### Solución

- Ingresamos a la pagina web
- Entramos a inspeccionar el codigo fuente
- Vemos que den las etiquetas de los CSS hay una referencia llamada secret/
- Entramos a http://saturn.picoctf.net:57831/secret/
- Vemos que la pagina nos dice que casi lo logramos
- Ingresamos al codigo fuente de esa pagina y vemos otra referencia llamada hidden/ 
- Entramos a view-source:http://saturn.picoctf.net:57831/secret/hidden/
- Vemos que existe otra referencia llamada superhidden/
- Ingresamos al siguiente link : view-source:http://saturn.picoctf.net:57831/secret/hidden/superhidden/
```
|   |
|---|
|<h1>Finally. You found me. But can you see me</h1>|
|<h3 class="flag">picoCTF{succ3ss_@h3n1c@10n_790d2615}</h3>|
```

Encontramos la bandera.
picoCTF{succ3ss_@h3n1c@10n_790d2615}
