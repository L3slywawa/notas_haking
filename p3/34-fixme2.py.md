#### Description

Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)

#### Hints 

Are equality and assignment the same symbol?

To view the file in the webshell, do: `$ nano fixme2.py`

To exit `nano`, press Ctrl and x and follow the on-screen prompts.

The `str_xor` function does not need to be reverse engineered for this challenge.

 ## SOLUCION
 
 
````
					//descargamos el programa
patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/5/fixme2.py     

2025-02-19 18:26:54 (279 MB/s) - 'fixme2.py' saved [1029/1029]

						//se muetsra el error que devemos corregir
						if flag == "":  
patoCosmico-picoctf@webshell:~$ python3 fixme2.py
  File "/home/patoCosmico-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?

							//abrimos el codigo para modificarlo
patoCosmico-picoctf@webshell:~$ nano fixme2.py 

							//corremos el programa correguido
patoCosmico-picoctf@webshell:~$ python3 fixme2.py
That is correct! Here's your flag: 

picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}

```