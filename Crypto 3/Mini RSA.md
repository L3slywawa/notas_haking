#### Description

What happens if you have a small exponent? There is a twist though, we padded the plaintext so that (M ** e) is just barely larger than N. Let's decrypt this: [ciphertext](https://mercury.picoctf.net/static/a24cf907007a19dbf30310acad0df9e5/ciphertext)

#### Hints 

12345

* RSA [tutorial](https://en.wikipedia.org/wiki/RSA_\(cryptosystem\))
* How could having too small of an `e` affect the security of this key?
* Make sure you don't lose precision, the numbers are pretty big (besides the `e` value)
* You shouldn't have to make _too_ many guesses
* `pico` is in the flag, but not at the beginning

### Solucion
Primero descargamos el archivo que nos aparece en nuestra descripción con el wget. Enseguida aplicamos un `cat` al archivo y nos mostrara los datos que necesitaremos para el código en python:

- `cat ciphertext`

Instalamos el gmpy2 con el siguiente comando ya que lo necesitaremos para el código que se realizará:

- `sudo apt install python3-gmpy2`

Y una vez finalizado el código lo ejecutamos con python3 enseguida del nombre del archivo de la siguiente manera:

- `python3 exp.py`

Y con esto nos mostrara nuestra respectiva flag.

Después en otra terminal ingresamos el siguiente comando para realizar el programa en python:

`nano exp.py`

Y escribimos el siguiente código con los datos que nos proporcionaron anteriormente.


````
from gmpy2 import iroot

n= 16157656843214630540782260519598878842336783177348929017407633211352136367960754624019502746024050951385898980874283>e= 3

c= 12200123185888718861325247578988844221745345580555937133090883049102739910735547326599771339806853708992578501219708>
for k in range(1, 100000):
     candidate = c + k * n
     m_root, exact = iroot(candidate, e)
     if exact:
         print(f'[+] Encontre raiz cubica exactak={k}')
         print('Entero desencriptado:', m_root)
         print('flag(ASCII):', bytes.fromhex(hex(m_root)[2:]))
         break
`````
Respuesta: picoCTF{e_sh0u1d_b3_lArg3r_a166c1e3}

