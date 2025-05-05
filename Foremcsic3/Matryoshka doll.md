#### Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/02_Matryoshka%20doll.md#description)

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/1b70cffdd2f05427fff97d13c496963f/dolls.jpg)

#### Hints

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/02_Matryoshka%20doll.md#hints)

- Wait, you can hide files inside files? But how do you find them?
- Make sure to submit the flag as picoCTF{XXXXX}

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/02_Matryoshka%20doll.md#soluci%C3%B3n)

Primero descargamos nuestro respectivo archivo y lo ubicamos en nuestra carpeta de linux, enseguida nos dirigimos a la terminal e instalamos el binwalk con el siguiente comando: `sudo apt install binwalk`

Para este reto se entraran a varias carpetas y es clave hacer un `ls` para saber en cual carpeta hay que ir entrando, y una vez que entremos hasta la ultima nos aparecerá el archivo del flag.txt y por lo tanto aplicamos un cat y con esto nos dará nuestra respectiva flag.

## Terminal de ejemplo:

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/02_Matryoshka%20doll.md#terminal-de-ejemplo)

```
lesly@Lesly:~$ wget https://mercury.picoctf.net/static/f6cc2560a70b1ea811c151accba5390f/dolls.jpg
--2025-05-05 10:32:50--  https://mercury.picoctf.net/static/f6cc2560a70b1ea811c151accba5390f/dolls.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 651635 (636K) [application/octet-stream]
Saving to: ‘dolls.jpg’

dolls.jpg                     100%[=================================================>] 636.36K   971KB/s    in 0.7s

2025-05-05 10:32:53 (971 KB/s) - ‘dolls.jpg’ saved [651635/651635]

lesly@Lesly:~$ binwalk -e dolls.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378955, uncompressed size: 383936, name: base_images/2_c.jpg
651613        0x9F15D         End of Zip archive, footer length: 22

lesly@Lesly:~$ cd base_images/
-bash: cd: base_images/: No such file or directory
lesly@Lesly:~$ ls
Dracula.yaml                  ende.py                  fixme2.tar.gz                pw.txt
Dracula.yaml:Zone.Identifier  ende.py:Zone.Identifier  flag.png                     pw.txt:Zone.Identifier
PSA232                        filler.txt               flag.txt.en                  shark2
SistemasOperativos            fixme1                   flag.txt.en:Zone.Identifier  snap
_dolls.jpg.extracted          fixme1.tar.gz            message.wav                  whitepages
color.                        fixme1.tar.gz.1          mystery                      whitepages.txt
dolls.jpg                     fixme2                   pico
lesly@Lesly:~$ cd _dolls.jpg.extracted/
lesly@Lesly:~/_dolls.jpg.extracted$ ls
4286C.zip  base_images
lesly@Lesly:~/_dolls.jpg.extracted$ cd base_images/
lesly@Lesly:~/_dolls.jpg.extracted/base_images$ binwalk -e 2_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196041, uncompressed size: 201443, name: base_images/3_c.jpg
383803        0x5DB3B         End of Zip archive, footer length: 22
383914        0x5DBAA         End of Zip archive, footer length: 22

lesly@Lesly:~/_dolls.jpg.extracted/base_images$ cd _2_c.jpg.extracted/
lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ cd base_images/
lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ binwalk -e 3_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77649, uncompressed size: 79806, name: base_images/4_c.jpg
201421        0x312CD         End of Zip archive, footer length: 22

lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ binwalk -e 3_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77649, uncompressed size: 79806, name: base_images/4_c.jpg
201421        0x312CD         End of Zip archive, footer length: 22

lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ cd _3_c.jpg.extracted/
lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted$ cd base_images/
lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ binwalk -e 4_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 62, uncompressed size: 81, name: flag.txt
79784         0x137A8         End of Zip archive, footer length: 22

lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg  _4_c.jpg.extracted
lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ cd  _4_c.jpg.extracted
lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ vi flag.txt

[1]+  Stopped                 vi flag.txt
lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ cat flag.txt
picoCTF{ac0072c423ee13bfc0b166af72e25b61}lesly@Lesly:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$

picoCTF{ac0072c423ee13bfc0b166af72e25b61}
```