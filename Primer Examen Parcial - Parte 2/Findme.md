## Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%202%20-%20Web/06_findme.md#description)

Help us test the form by submiting the username as `test` and password as `test!` The website running [here](http://saturn.picoctf.net:57004/).

## Hints

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%202%20-%20Web/06_findme.md#hints)

- any redirections?

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%202%20-%20Web/06_findme.md#soluci%C3%B3n)

Iniciamos nuestra instancia y copiamos el link que nos proporcionaron, después nos dirigimos a la aplicación de **Burp Suite Community Edition**, nos dirigimos a **proxy** y seleccionamos **open browser** y en el nuevo navegador pegamos el link anterior, una vez ahí, iniciamos sesión con: `username:test and password:test!` y habilitamos el botón de `Interception off` y damos enter al navegador donde ingresamos el link.

Enseguida damos clic al botón `Forward` y nos aparece nuestro primer encriptado en base64, lo seleccionamos y automáticamente se desencripta y nos muestra la primera parte de nuestra flag, como se observa en la imagen siguiente:

![[Pasted image 20250414155315.png]]

Después volvemos a dar `Forward` y nos sale nuestra segunda parte de encriptado base64 y automáticamente nos muestra el resto de nuestra respectiva flag, juntamos las dos partes y nos da nuestro resultado.

picoCTF{proxies_all_the_way_3d9e3697}