#### Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/04_hideme.md#description)

Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/258/flag.png).

#### Hints

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/04_hideme.md#hints)

- (None)

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/04_hideme.md#soluci%C3%B3n)

Primero descargamos nuestro respectivo archivo y lo ubicamos en nuestra carpeta de linux.

Ingresamos a nuestra terminal de linux e ingresamos en las siguientes direcciones de carpeta para identificar en cuales carpetas entrar y hacer que la imagen nos muestre la bandera:

- `cd _flag.png.extracted`
- `cd secret`

y después en la ultima carpeta ubicamos nuestra flag en imagen, por lo tanto instalamos `lrzsz` con el siguiente comando:

Y aplicamos un `sz flg.png` y con esto nos abrirá nuestra imagen con la flag dentro.

## Terminal de ejemplo:

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/04_hideme.md#terminal-de-ejemplo)

```
 binwalk flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2876, uncompressed size: 3029, name: secret/flag.png
42915         0xA7A3          End of Zip archive, footer length: 22

jazmin@DESKTOP-1CBQJ6D:~/FSI/hideme$ binwalk -e flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2876, uncompressed size: 3029, name: secret/flag.png
42915         0xA7A3          End of Zip archive, footer length: 22
 ls
_flag.png.extracted  flag.png  flag.png:Zone.Identifier
 cd _flag.png.extracted
 ls
29  29.zlib  9B3B.zip  secret

 cd secret
 ls
 
flag.png
sz flg.png

Command 'sz' not found, but can be installed with:

sudo apt install lrzsz

 sudo apt install lrzsz
 sz flg.png
```


picoCTF{Hiddinng_An_imag3_within_@n_ima9e_sdffsd8}