

## Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%201%20-%20General%20Skills/01_FANTASY%20CTF.md#description)

Play this short game to get familiar with terminal applications and some of the most important rules in scope for picoCTF. Connect to the program with netcat: `$ nc verbal-sleep.picoctf.net 57327`

## Hints 1

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%201%20-%20General%20Skills/01_FANTASY%20CTF.md#hints-1)

- When a choice is presented like [a/b/c], choose one, for example: `c` and then press Enter.

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%201%20-%20General%20Skills/01_FANTASY%20CTF.md#soluci%C3%B3n)

Copiamos el nc que se nos proporciona `nc verbal-sleep.picoctf.net 57327`, enseguida lo pegamos en una terminal de ubuntu o en el webshell del PicoCTF, aquí mismo nos menciona que debemos dar **Enter** para continuar y lo hacemos varias veces hasta que nos aparece una sección de preguntas: **Options: A) _Register multiple accounts_ B) _Share an account with a friend_ C) _Register a single, private account_ [a/b/c] > a** y nos pedirá seleccionar una respuesta, y escribimos la letra `a`.

Una vez echo esto seguimos dando **Enter**, hasta que nos vuelve a dar otra sección de preguntas: **Options: A) _Play the game_ B) _Search the Ether for the flag_ [a/b] > a** y nuevamente escribimos la letra `a` y continuamos dando **Enter**. Y después de varios **Enter** nos muestra nuestra respectiva flag.

Respuesta: 
picoCTF{m1113n1um_3d1710n_9a3a7333} 



