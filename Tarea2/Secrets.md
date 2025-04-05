#### Description

We have several pages hidden. Can you find the one with the flag?

Additional details will be available after launching your challenge instance.

Solucion:
vemos el codigo fuente y hay un .css que dice sicret vamos al link soloooo que asta donde dice secret.

````
original: http://saturn.picoctf.net:61518/secret/assets/index.css
otro    : http://saturn.picoctf.net:61518/secret/
`````
 nos muestra otra pagina vemos su codigo fuente y vemos un link hidden
 asi que al link secret le agregamos /hidden
 ````
 view-source:http://saturn.picoctf.net:61518/secret/hidden/
`````

ahora a este link lo buscamos desde http
view-source :    http://saturn.picoctf.net:61518/secret/hidden/

vemos su fuente y hay un superhidden 
-> http://saturn.picoctf.net:61518/secret/hidden/superhidden/

y en el codigo fuente de esta esta la bandera 

picoCTF{succ3ss_@h3n1c@10n_790d2615}