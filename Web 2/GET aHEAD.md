#### Description

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:45028/](http://mercury.picoctf.net:45028/)

#### Hints 

1-Maybe you have more than 2 choices
2-Check out tools like Burpsuite to modify your requests and look at the responses

````
This message is shown once a day. To disable it please create the
/home/lesly/.hushlogin file.
lesly@Lesly:~$ curl -I http://mercury.picoctf.net:45028/index.php
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_775f2530}
Content-type: text/html; charset=UTF-8
```