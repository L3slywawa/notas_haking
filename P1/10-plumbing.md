#### Description

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.

### solucion


````
	patoCosmico-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 4427 | grep pico 
picoCTF{digital_plumb3r_5ea1fbd7}
```