#### Description

If you want to hash with the best, beat this test!

Additional details will be available after launching your challenge instance.
#### Hints 

* You can use a commandline tool or web app to hash text
* Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

#### Solución


En nuestra consola vamos a copiar y pegar lo siguiente(lo que nos dan en la instancia) despues nos dara una palabra entre comillas simples, esa palabra la vamos a copiar y la pegaremos en la siguiente pagina.
[https://www.md5hashgenerator.com/](https://www.md5hashgenerator.com/)

y vamos a copiar el texto que se encuentra en el apartado de MD5 HASH y eso lo llevaremos a nuestra consola, luego nos seguira dando aproximadamente otras 2 palabras con las cuales haremos el mismo procedimimento que hicimos antes hasta que nos de la bandera.

````

patoCosmico-picoctf@webshell:~$ nc saturn.picoctf.net 52635
Please md5 hash the text between quotes, excluding the quotes: 'Cinco de Mayo'
Answer: 
3b55fa8f34aae6b045ccec7f9b5d4c89
3b55fa8f34aae6b045ccec7f9b5d4c89
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'a used car lot'
Answer: 
1a78bc064f8df8b4192ce5f8972c9b80
1a78bc064f8df8b4192ce5f8972c9b80
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'construction workers'
Answer: 
00ae932c1c12ee89427c3efeeecf9533
00ae932c1c12ee89427c3efeeecf9533
Correct.

picoCTF{4ppl1c4710n_r3c31v3d_3eb82b73}
```