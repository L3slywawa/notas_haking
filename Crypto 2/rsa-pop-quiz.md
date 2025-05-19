#### Description

Class, take your seats! It's PRIME-time for a quiz... `nc jupiter.challenges.picoctf.org 18821`

#### Hints 

* [RSA info](https://simple.wikipedia.org/wiki/RSA_algorithm)
  
  ## Solucion:
  
  creamos este código en Python que hace los cálculos que nos pide el link cuando entramos en este, tomando en cuenta que cada persona tiene solo dos diferencias:
  el puerto 18821
````
jupiter.challenges.picoctf.org",18821
`````
y el "c" o código encriptado en la pregunta 7  y 8  

el codigo:
````

from pwn import *

r = remote("jupiter.challenges.picoctf.org",18821)
print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
q = 60413
p = 76753
n = p * q
print('n='+str(n))
r.sendline(str(n).encode())

print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
p = 54269
n = 5051846941
q = n // p
print('q='+str(q))
r.sendline(str(q).encode())

print(r.recvuntil(b'):').decode())
r.sendline(b'N')

print(r.recvuntil(b'):').decode())

print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
q = 66347
p = 12611
t = (p-1) * (q-1)
print('t='+str(t))
r.sendline(str(t).encode())

print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
m = 6357294171489311547190987615544575133581967886499484091352661406414044440475205342882841236357665973431462491355089>e = 3
n = 2912946360932632255952112313622207878058545120814913854779912108362233325064667876776912624818220747852788102511633>c = pow(m, e, n)
print('c='+str(c))
r.sendline(str(c).encode())

print(r.recvuntil(b'):').decode())
r.sendline(b'N')

print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
q =  920920768058925337397247226026686758406710930085202415481919142153998240203720761864607682068149144238022303984109>p = 9784677531239280103722439697701261584843319964010578611975704709875799827300974112882193127707455573181328942389138>e = 65537
t = (p-1) * (q-1)
d = pow(e, -1, t)
print('d='+str(d))
r.sendline(str(d).encode())

print(r.recvuntil(b'):').decode())
r.sendline(b'Y')
print(r.recvuntil(b': ').decode())
p = 1531430422725278687984126124172044341569351468742829909423866940204628619180686845612817635770347066006083876991480>c = 1343329094968053237401386744126315463470581503738278934194790502557390597439502814650316215547726098952087017563825>
e = 65537
n = 2395293735264352745137922751642837770500489450856630431317788019166217706187899379893849681812098781704953836520667>q = n // p
t = (p-1) * (q-1)
d = pow(e, -1, t)
m = pow(c, d, n)
print('m='+str(m))
r.sendline(str(m).encode())

print(r.recvall().decode())
flag = bytes.fromhex(hex(m)[2:]).decode()

print(flag)
`````

solucion
picoCTF{wA8_th4t$_ill3aGal..oa2d2239b}