#### Description

Using a Secure Shell (SSH) is going to be pretty important.
Additional details will be available after launching your challenge instance.

### HINTS

1.- https://linux.die.net/man/1/ssh
2.- You can try logging in 'as' someone with `<user>`@titan.picoctf.net
3.- How could you specify the port?
4.- member, passwords are hidden when typed into the shell



````
Using a Secure Shell (SSH) is going to be pretty important.Can you `ssh` as `ctf-player` to `titan.picoctf.net` at port `50043` to get the flag?You'll also need the password `1db87a14`. If asked, accept the fingerprint with `yes`.If your device doesn't have a shell, you can use: [https://webshell.picoctf.org](https://webshell.picoctf.org/)If you're not sure what a shell is, check out our Primer: [https://primer.picoctf.com/#_the_shell](https://primer.picoctf.com/#_the_shell)
<//
````````


## SOLUCION

usamos este comando de acuerdo a la información anterior

```
ssh -2 ctf-player@titan.picoctf.net -p 50043
```
````

patoCosmico-picoctf@webshell:~$ ssh -2 ctf-player@titan.picoctf.net -p 50043
The authenticity of host '[titan.picoctf.net]:50043 ([3.139.174.234]:50043)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:50043' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password:

				//ingresamos la contraseña dada anteriormente
				// y nos dara la bandera

Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_45a48857}
Connection to titan.picoctf.net closed.
patoCosmico-picoctf@webshell:~$ 
`````