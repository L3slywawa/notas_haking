#### Description

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/213/disk.flag.img.gz)


## solucion

````
$ wget https://artifacts.picoctf.net/c/213/disk.flag.img.gz
--2025-05-07 13:06:44--  https://artifacts.picoctf.net/c/213/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.100, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 44360922 (42M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz              100%[=================================================>]  42.31M  18.6MB/s    in 2.3s

2025-05-07 13:06:47 (18.6 MB/s) - ‘disk.flag.img.gz’ saved [44360922/44360922]

lesly@Lesly:~/anterior$ gzip -d disk.flag.img.gz
lesly@Lesly:~/anterior$ mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
lesly@Lesly:~/anterior$ ^C
lesly@Lesly:~/anterior$ fls disk.flag.img -o 411648 472
r/r 1875:       .ash_history
r/r * 1876(realloc):    flag.txt
r/r 1782:       flag.txt.enc
lesly@Lesly:~/anterior$ icat disk.flag.img -o 411648 1782
Salted__�ށ��e��B�J�c�$QE&$��4jM�KGeE�1�^Ȥ7� ���؎$�'%lesly@Lesly:~/anterior$
lesly@Lesly:~/anterior$
lesly@Lesly:~/anterior$ icat disk.flag.img -o 411648 1782 > flag.txt.enc
lesly@Lesly:~/anterior$ icat disk.flag.img -o 411648 1875
touch flag.txt
nano flag.txt
apk get nano
apk --help
apk add nano
nano flag.txt
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
lesly@Lesly:~/anterior$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
40678D22897F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:124:
lesly@Lesly:~/anterior$ cat flag.txt
picoCTF{h4un71ng_p457_5113beab}lesly@Lesly:~/anterior$
```