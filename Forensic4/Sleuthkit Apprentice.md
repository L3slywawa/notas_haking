#### Description

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/137/disk.flag.img.gz)

## solucion

````

wget https://artifacts.picoctf.net/c/137/disk.flag.img.gz

 gzip -d disk.flag.img.gz

 ls -lah disk.flag.img

mmls disk.flag.img

fls disk.flag.img -o 360448 -r

 icat disk.flag.img -o 360448 2371

picoCTF{by73_5urf3r_adac6cb4}
```