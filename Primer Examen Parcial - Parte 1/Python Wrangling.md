## Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%201%20-%20General%20Skills/03_Python%20Wrangling.md#description)

Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py) using [this password](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/pw.txt) to get [the flag](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/flag.txt.en)?

## Hints 1 2

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%201%20-%20General%20Skills/03_Python%20Wrangling.md#hints-1-2)

- Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py`
- `$ man python`

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Primer%20Examen%20Parcial/Parte%201%20-%20General%20Skills/03_Python%20Wrangling.md#soluci%C3%B3n)

Primero descargamos los archivos correspondientes los cuales son:

- **ende.py**
- **flag.txt.en**
- **pw.txt**

Y los ubicamos en nuestra carpeta de linux, enseguida ingresamos en nuestra terminal el siguiente comando: `python3 ende.py -d flag.txt.en`

Después pide la contraseña, la cual se ubica en el archivo `pw.txt` Y con esto nos muestra nuestra respectiva flag:

## Terminal de ejemplo:
````
 cd FIS/
/FIS$ python3 ende.py -d flag.txt.en
ac9bd0ffac9bd0ffac9bd0ffac9bd0ff

picoCTF{4p0110_1n_7h3_h0us3_ac9bd0ff}
```