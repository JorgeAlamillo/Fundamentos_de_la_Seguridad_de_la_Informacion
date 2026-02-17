### Serpentine

### Descripción

Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/37/serpentine.py)
### Solución

### Solucion 1 - Usando Consola

```
wget -q https://artifacts.picoctf.net/c/37/serpentine.py
nano serpentine.py

"entramos a serpentine py, y modificamos el else de la opcionn b para que al seleccionar la opcion b nos imprima la bandera."

    elif choice == 'b':
      print_flag()
      print('\nOops! I must have misplaced the print_flag function! Check my source code!\n\n')
      

python serpentine.py 

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_8e47d128}

```

