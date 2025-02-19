#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## HINTS
To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`

To exit `bvi` type `:q` and press enter.

The `str_xor` function does not need to be reverse engineered for this challenge.

### SOLUCION


descargar archivos
````

`patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.py`
`-`
`2025-02-19 19:40:22 (549 MB/s) - 'level3.py' saved [1337/1337]`

`patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc`

`2025-02-19 19:40:35 (41.2 MB/s) - 'level3.flag.txt.enc' saved [31/31]`

`patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin`

`2025-02-19 19:40:47 (12.3 MB/s) - 'level3.hash.bin' saved [16/16]`

`````

#### abres el documento, y cambias la posición de las posibles contraseñas

hacemos un for que pruebe las contraseñas asta la correcta
````

pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]


def level_3_pw_check():
######    user_pw = input("Please enter correct password for flag: ")
   for user_pw in pos_pw_list:
       user_pw_hash = hash_pw(user_pw)
    
       if( user_pw_hash == correct_pw_hash ):
           print("Welcome back... your flag, user:")
           decryption = str_xor(flag_enc.decode(), user_pw)
           print(decryption)
           return
       print("That password is incorrect")



level_3_pw_check()
``````
```
```

Probamos el código y nos da la bandera.
````

patoCosmico-picoctf@webshell:~$ python3 level3.py
That password is incorrect
That password is incorrect
Welcome back... your flag, user:

picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```
