#### Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/03_Redaction%20gone%20wrong.md#description)

Now you DON’T see me. This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

#### Hints

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/03_Redaction%20gone%20wrong.md#hints)

- How can you be sure of the redaction?

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/03_Redaction%20gone%20wrong.md#soluci%C3%B3n)

Primeramente descargamos el link del enlace que se nos proporciona y damos clic derecho y seleccionamos `Guardar enlace como...` y lo descargamos como pdf.

Enseguida abrimos el archivo y copiamos el contenido que lleva dentro y lo pegamos en un bloc de notas y con esto nos mostrara nuestra respectiva flag, ya que se entraba escondida dentro del pdf.

## Contenido del pdf copiado

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/03_Redaction%20gone%20wrong.md#contenido-del-pdf-copiado)

```
Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.
Breakdown - Just painted over in MS word.
Cost Benefit Analysis
Credit Debit
This is not the flag, keep looking
Expenses from the
picoCTF{C4n_Y0u_S33_m3_fully}
Redacted document.
```

### Respuesta: picoCTF{C4n_Y0u_S33_m3_fully}