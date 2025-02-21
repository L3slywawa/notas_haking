### Description

I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/75/challenge.zip)

### Hint

[](https://github.com/Tiitania/hacking-nodes-2025/blob/main/PicoCTF/Tarea%201/Commitment%20Issues.md#hint)

- Version control can help you recover files if you change or lose them!
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)
- you can 'checkout' commits to see the files inside them
Solucion

````
patoCosmico-picoctf@webshell:~/drop-in/drop-in$ wget https://artifacts.picoctf.net/c_titan/137/challenge.zip
			 'challenge.zip' 

patoCosmico-picoctf@webshell:~/drop-in/drop-in$ ls
challenge.zip  drop-in  flag.py
patoCosmico-picoctf@webshell:~/drop-in/drop-in$ cd drop-in/
patoCosmico-picoctf@webshell:~/drop-in/drop-in/drop-in$ ls
message.txt
patoCosmico-picoctf@webshell:~/drop-in/drop-in/drop-in$ ls -la

patoCosmico-picoctf@webshell:~/drop-in/drop-in/drop-in$ cat message.txt
TOP SECRET
patoCosmico-picoctf@webshell:~/drop-in/drop-in/drop-in$ git reflog

patoCosmico-picoctf@webshell:~/drop-in/drop-in/drop-in$ git checkout ea859bf
Note: switching to 'ea859bf'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ea859bf create flag
patoCosmico-picoctf@webshell:~/drop-in/drop-in/drop-in$ cat message.txt
picoCTF{s@n1t1z3_cf09a485}
```