#### Description

What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/161/challenge.zip)

SOLUCION

````
picoCTF{t1m3m@ch1n3_8defe16a}
`````

CODIGO ````


```
 
patoCosmico-picoctf@webshell:~$ cat message.txt
cat: message.txt: No such file or directory
patoCosmico-picoctf@webshell:~$ cd drop-in/
patoCosmico-picoctf@webshell:~/drop-in$ cat message.txt
This is what I was working on, but I'd need to look at my commit history to know why...patoCosmico-picoctf@webshell:~/drop-in$   
patoCosmico-picoctf@webshell:~/drop-in$ cat message.txt
This is what I was working on, but I'd need to look at my commit history to know why...patoCosmico-picoctf@webshell:~/drop-in$ git checkout message.txt
Updated 1 path from the index
patoCosmico-picoctf@webshell:~/drop-in$ git log


commit 10228f3d6437701ef5aaac04213757031f30ebec (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:24 2024 +0000
```
