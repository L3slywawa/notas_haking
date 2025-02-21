### Description

Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/73/challenge.zip)

### Hint

[](https://github.com/Tiitania/hacking-nodes-2025/blob/main/PicoCTF/Tarea%201/Blame%20Game.md#hint)

- In collaborative projects, many users can make many changes. How can you see the changes within one file?
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
- You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.


SOLUCION


````
commit 2466febd40004b9ca644ce924181d07e23dcfaeb (HEAD)
Author: picoCTF{@sk_th3_1nt3rn_cfca95b2} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:06 2024 +0000

    optimize file size of prod code
`````

código para llegar aquí

````
patoCosmico-picoctf@webshell:~$ wget 
patoCosmico-picoctf@webshell:~$ unzip challenge.zip.1


patoCosmico-picoctf@webshell:~/drop-in$ cat message.py
print("Hello, World!"
patoCosmico-picoctf@webshell:~/drop-in$ git reflog

patoCosmico-picoctf@webshell:~/drop-in$ cat message.py
print("Hello, World!")
patoCosmico-picoctf@webshell:~/drop-in$ git reflog

[2]+  Stopped                 git reflog
patoCosmico-picoctf@webshell:~/drop-in$ 
patoCosmico-picoctf@webshell:~/drop-in$ git checkout 2466feb

					//aqui checamos con el codigo de optimisacion
					ya que el secreto no funciono

patoCosmico-picoctf@webshell:~/drop-in$ cat message.py
print("Hello, World!"
patoCosmico-picoctf@webshell:~/drop-in$ git log
```