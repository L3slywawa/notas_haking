#### Description

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/51d68e61bb41207a55f24e753f07c5a3/values)

#### Hints 

1

Bits are expensive, I used only a little bit over 100 to save money

````
c: 62324783949134119159408816513334912534343517300880137691662780895409992760262021
n: 1280678415822214057864524798453297819181910621573945477544758171055968245116423923
e: 65537



`````
factorisamos 

````
[1899107986527483535344517113948531328331](https://factordb.com/index.php?id=1100000002524332350)


[1899107986527483535344517113948531328331](https://factordb.com/index.php?id=1100000002524332350)
`````

bandera:
picoCTF{sma11_N_n0_g0od_05012767}