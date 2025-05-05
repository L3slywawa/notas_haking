#### Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/05_WebNet1.md#description)

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

#### Hints

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/05_WebNet1.md#hints)

- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/05_WebNet1.md#soluci%C3%B3n)

Primero descargamos nuestro respectivo archivo y lo ubicamos en nuestra carpeta de linux, enseguida nos dirigimos a la terminal e ingresamos el siguiente comando que nos dirigirá al **WireShark** en el cual nos ayudara a resolver el reto:

`wireshark capture.pcap &`

Enseguida descargamos la llave privada, nos dirigimos a `Edit` y a `Preferences`, enseguida de eso vamos a `Protocols` y buscamos `TLS` y nos da la opción de subir una llave y ahí importamos nuestro archivo llamado `picopico.key` y una vez subido se pone en verde algunos y esto significa que esta desencriptado.

Después nos dirigimos al paquete 47 y nos dirigimos a `File`, en `Export Objects` y seleccionamos `HTTP` y seleccionamos el paquete 91 para descargar la imagen y la ubicamos en nuestra carpeta de linux.

Después nos dirigimos nuevamente a la terminal e ingresamos el siguiente comando y con esto nos dará nuestra respectiva flag.

`strings vulture.jpg`

## Terminal de ejemplo:

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/05_WebNet1.md#terminal-de-ejemplo)

```
 cd FSI/
 cd WebNet1/
 wireshark capture.pcap &
[1] 698

nl80211 not found.
21:24:03.995     Main Warn FIX Add drag reordering to UAT dialog

 ls
'capture(1).pcap:Zone.Identifier'   capture.pcap   picopico.key   picopico.key:Zone.Identifier   vulture.jpg

 strings vulture.jpg
JFIF
Exif
picoCTF{honey.roasted.peanuts}
ICC_PROFILE
lcms
mntrRGB XYZ
9acspAPPL
-lcms
desc
^cprt
wtpt
```

### Respuesta: picoCTF{honey.roasted.peanuts}