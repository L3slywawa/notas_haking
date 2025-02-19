#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) ( https://artifacts.picoctf.net/c/11/level1.py )  and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc)   (https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.

#### Hints 

To view the file in the webshell, do: `$ nano level1.py`

To exit `nano`, press Ctrl and x and follow the on-screen prompts.

The `str_xor` function does not need to be reverse engineered for this challenge.


SOLUTION

1e1a
````

			//descargamos el archivo
			
patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.py

				//nombre del archovo
Saving to: 'level1.py.2'

				// abrimos y vemos el codigo 
patoCosmico-picoctf@webshell:~$ nano level1.py


		// en el codigo comparava una conraseña 
		si escribiamos " 1e1a "  daira la llave


		//corremos el programa
patoCosmico-picoctf@webshell:~$ python3 level1.py.2

			// damos la contraseña 
Please enter correct password for flag: 1e1a

		//nos da la llave
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
patoCosmico-picoctf@webshell:~$ 
```