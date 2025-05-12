#### Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/06_CanYouSee.md#description)

How about some hide and seek? Download this file [here](https://artifacts.picoctf.net/c_titan/5/unknown.zip).

#### Hints

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/06_CanYouSee.md#hints)

- How can you view the information about the picture?
- If something isn't in the expected form, maybe it deserves attention?

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/06_CanYouSee.md#soluci%C3%B3n)

Primeramente descargamos nuestro respectivo archivo y lo ubicamos en nuestra carpeta de linux.

Enseguida descomprimimos el archivo que es un zip con el siguiente comando:

`unzip unknown.zip`

Después ingresamos el siguiente comando para que nos muestre los tipos de archivo que vienen dentro:

`exiftool ukn_reality.jpg`

En la parte de `Attribution URL` y copiamos el cifrado y lo ingresamos en un link de cyberchef y lo pasamos a `from base64` para transformarlo a nuestra respectiva flag.

## Terminal de ejemplo:

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/06_CanYouSee.md#terminal-de-ejemplo)

```
unzip unknown.zip
Archive:  unknown.zip

te dara unos numeros raros y los mandas a CiverChef

FROM BASE64 
input :
cGljb0NURntNRTc0RDQ3QV9ISUREM05fYTZkZjhkYjh9Cg

TO DECIMAL

output:
picoCTF{ME74D47A_HIDD3N_a6df8db8}
```
