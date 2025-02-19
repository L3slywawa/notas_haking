#### Description

Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/36/serpentine.py)


HINTS
1.-Try running the script and see what happens
2.- In the webshell, try examining the script with a text editor like `nano`
3.- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4.- The `str_xor` function does not need to be reverse engineered for this challenge.

SOLUCION

primero descargar el programa
````
patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/36/serpentine.py
Saving to: 'serpentine.py'


`````

luego abres el programa y modificas cuando abre la bandera
para que si la abra realmente

````

patoCosmico-picoctf@webshell:~$ nano serpentine.py


    elif choice == 'b':
      print_flag()


````````

y se debería mostrar sin problemas 
```
patoCosmico-picoctf@webshell:~$ python3 serpentine.py

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

picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}


a) Print encouragement
b) Print flag
c) Quit

`````
