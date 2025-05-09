
#### Description

Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.
````
 wget ´https://artifacts.picoctf.net/c/164/disk.img.gz´
´https://artifacts.picoctf.net/c/164/disk.img.gz´: Scheme missing.
lesly@Lesly:~/anterior$ wget https://artifacts.picoctf.net/c/164/disk.img.gz
--2025-05-07 12:48:28--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.61, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                   100%[=================================================>]  28.34M  13.7MB/s    in 2.1s

2025-05-07 12:48:31 (13.7 MB/s) - ‘disk.img.gz’ saved [29714372/29714372]

lesly@Lesly:~/anterior$ ls -lah disk.img.gz
-rw-r--r-- 1 lesly lesly 29M Aug  4  2023 disk.img.gz
lesly@Lesly:~/anterior$ gzip -d disk.img.gz
lesly@Lesly:~/anterior$ ls -lsh disk.img.gz
ls: cannot access 'disk.img.gz': No such file or directory
lesly@Lesly:~/anterior$ ls
disk.img
lesly@Lesly:~/anterior$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
lesly@Lesly:~/anterior$ nc nc saturn.picoctf.net 64840
nc: port number invalid: saturn.picoctf.net
lesly@Lesly:~/anterior$
lesly@Lesly:~/anterior$ nc saturn.picoctf.net 64840
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}
```