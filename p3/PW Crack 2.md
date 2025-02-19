#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.

#### Hints 

Does that encoding look familiar?

The `str_xor` function does not need to be reverse engineered for this challenge.


SOLUCION

```
			//primero se descargan los archivos //
			
patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.py

NOMBRE: 'level2.py.1'

patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc

NOMBRE: 'level2.flag.txt.enc.1'


			//luego se abre el codigo para verlo
			
patoCosmico-picoctf@webshell:~$ nano level2.py.1
```


ya abierto se muestra el código que usa archivos chrs, asi que los Interpretamos

````
def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")


EL VALOR INTERPRETADO:   "39ce"
````


así que ponemos este valor como la contraseña  y dará la vadera.
```
patoCosmico-picoctf@webshell:~$ python3 level2.py.1
Please enter correct password for flag: 39ce
Welcome back... your flag, user: 

picoCTF{tr45h_51ng1ng_502ec42e}
