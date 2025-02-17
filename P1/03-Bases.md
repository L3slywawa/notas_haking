#### Description

What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

# Solución
cyberchef 
```
INPUT 
`bDNhcm5fdGgzX3IwcDM1`

From base64

OUTPUT
l3arn_th3_r0p35

#Solucion 2 
patoCosmico-picoctf@webshell:~$ echo bDNhcm5fdGgzX3IwcDM1 | base64 -d
l3arn_th3_r0p35  patoCosmico-picoctf@webshell:~$ 

picoCTF{l3arn_th3_r0p35}
```