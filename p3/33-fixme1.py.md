#### Description

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)


#### Hints

To view the file in the webshell, do: `$ nano fixme1.py`

To exit `nano`, press Ctrl and x and follow the on-screen prompts.

The `str_xor` function does not need to be reverse engineered for this challenge.


````
patoCosmico-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/25/fixme1.py
--2025-02-19 01:13:43--  https://artifacts.picoctf.net/c/25/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py.1'

fixme1.py.1          100%[======================>]     837  --.-KB/s    in 0s      

2025-02-19 01:13:43 (13.7 MB/s) - 'fixme1.py.1' saved [837/837]

patoCosmico-picoctf@webshell:~$ python3 fixme1.py
  File "/home/patoCosmico-picoctf/fixme1.py", line 20
    print('That is correct! Hers your flag: ' + flag)
IndentationError: unexpected indent
patoCosmico-picoctf@webshell:~$ nano fixme1.py
patoCosmico-picoctf@webshell:~$ python3 fixme1.py
  File "/home/patoCosmico-picoctf/fixme1.py", line 20
    print('That is correct! Hers your flag: ' + flag)
IndentationError: unexpected indent
patoCosmico-picoctf@webshell:~$ nano fixme1.py
patoCosmico-picoctf@webshell:~$ python3 fixme1.py
That is correct! Hers your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```