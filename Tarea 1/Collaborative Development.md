My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/176/challenge.zip)

### Hint

- `git branch -a` will let you see available branches
- How can file 'diffs' be brought to the main branch? Don't forget to `git config`!
- Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.


````
atoCosmico-picoctf@webshell:~/drop-in$ rm -rf challenge.zip
patoCosmico-picoctf@webshell:~/drop-in$ ls
drop-in  flag.py  message.py
patoCosmico-picoctf@webshell:~/drop-in$ cd drop-in/
patoCosmico-picoctf@webshell:~/drop-in/drop-in$ ls
flag.py
patoCosmico-picoctf@webshell:~/drop-in/drop-in$ cat flag.py
print("Printing the flag...")
patoCosmico-picoctf@webshell:~/drop-in/drop-in$ git branch -a
[4]+  Stopped                 git branch -a
patoCosmico-picoctf@webshell:~/drop-in/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
patoCosmico-picoctf@webshell:~/drop-in/drop-in$ ls
flag.py
patoCosmico-picoctf@webshell:~/drop-in/drop-in$ cat flag.py
print("Printing the flag...")


print("picoCTF{t3@mw0rk_",


end='')patoCosmico-picoctf@webshell:~/drop-in/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
patoCosmico-picoctf@webshell:~/drop-in/drop-in$ cat flag.py
print("Printing the flag...")


print("m@k3s_th3_dr3@m_",


end='')patoCosmico-picoctf@webshell:~/drop-in/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
patoCosmico-picoctf@webshell:~/drop-in/drop-in$ cat flag.py
print("Printing the flag...")



print("w0rk_e4b79efb}")



```
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_e4b79efb}
