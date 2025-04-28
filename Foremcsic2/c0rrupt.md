#### Description

We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
#### Hints 

* Try fixing the file header+

## solucion


````
 wget https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
 
lesly@Lesly:~$ sudo apt install ncurses-hexedit


lesly@Lesly:~$ hexeditor flag.png
lesly@Lesly:~$ pngcheck flag.png

lesly@Lesly:~$ hexeditor flag.png

picoCTF{c0rrupt10n_1847995}
```