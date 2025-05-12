#### Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/05_Scan%20Surprise.md#description)

I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead? You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/3/challenge.zip)

The same files are accessible via SSH here: `ssh -p 56374 ctf-player@atlas.picoctf.net` Using the password `6dd28e9b`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

#### Hints

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/05_Scan%20Surprise.md#hints)

- QR codes are a way of encoding data. While they're most known for storing URLs, they can store other things too.
- Mobile phones have included native QR code scanners in their cameras since version 8 (Oreo) and iOS 11.
- If you don't have access to a phone, you can also use zbar-tools to convert an image to text.

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/05_Scan%20Surprise.md#soluci%C3%B3n)

Primero descargamos nuestro respectivo archivo y lo ubicamos en nuestra carpeta de linux.

Enseguida iniciamos nuestra instancia para los datos que necesitaremos.

Ingresamos a nuestra terminal de linux y pegamos el ssh de nuestra instancia y la contraseña.

Una vez dentro nos mostrara una imagen de qr, entonces nos damos cuenta de que dentro hay una flag y aplicamos un `zbarimg` y nos mostrara nuestra respectiva flag.

## Terminal de ejemplo:

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/05_Scan%20Surprise.md#terminal-de-ejemplo)

```
 ssh -p 56374 ctf-player@atlas.picoctf.net

 ls
flag.png
 zbarimg flag.png

picoCTF{p33k_@_b00_d4ca652e}
```