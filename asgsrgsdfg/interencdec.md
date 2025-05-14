# Descripción

[](https://github.com/AsumomezaC/Hacking-notes-2025/blob/main/PicoCTF/crypto/a16/08%20-%20interencdec.md#descripci%C3%B3n)

Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/1/enc_flag).

# Pistas

[](https://github.com/AsumomezaC/Hacking-notes-2025/blob/main/PicoCTF/crypto/a16/08%20-%20interencdec.md#pistas)

Engaging in various decoding processes is of utmost importance

# Solución

[](https://github.com/AsumomezaC/Hacking-notes-2025/blob/main/PicoCTF/crypto/a16/08%20-%20interencdec.md#soluci%C3%B3n)

Comenzamos viendo que el problema tiene dos conceptos clave: [[Codificación Base 64]] y [[Cifrado César]]. Suponemos que combinarlos dará la solución.

Descargamos el archivo con [[wget]].

```shell
 wget https://artifacts.picoctf.net/c_titan/1/enc_flag

2025-05-12 18:24:06 (19.8 MB/s) - 'enc_flag' saved [73/73]
```

Vemos su contenido con [[Strings]].

```
lesly@Lesly:~/anterior$ cat enc_flag
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyZzBOMm8yYXpZNWZRPT0nCg==
```

Su contenido parece estar en [[Codificación Base 64]], por lo que nos apoyamos de [cyberchef](https://cyberchef.org/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)) para [[Decodificador|decodificarlo]].

b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ=='

Parece que nos dio otro texto en [[Codificación Base 64]] -por la b' y los caractéres-, por lo que repetimos el proceso.

d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2g0N2o2azY5fQ=='

Ahora obtenemos algo mucho más parecido a la bandera, por lo que ahora probamos suerte con el [[Cifrado César]] usando una [herramienta online](https://www.dcode.fr/cifrado-cesar). Y obtenemos la bandera.

picoCTF{caesar_d3cr9pt3d_a47c6d69}