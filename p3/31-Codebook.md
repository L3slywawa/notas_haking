#### Description

Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)


#### Hints 

1-On the webshell, use `ls` to see if both files are in the directory you are in
2-The `str_xor` function does not need to be reverse engineered for this challenge.

SOLUCION
````
		     //se instalan ambos archivos
patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/code.py

patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/codebook.txt
2025-02-19 00:56:03 (20.2 MB/s) - 'codebook.txt' saved [27/27]
				//corres el programam
patoCosmico-picoctf@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_d9aa2df2}

```