#### Description

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/ac394d24f88e51a09cc909687cf6d853/dds1-alpine.flag.img.gz)

#### Hints 

* Have you ever used `file` to determine what a file was?
* Relevant terminal-fu in picoGym: https://play.picoctf.org/practice/challenge/85
* Mastering this terminal-fu would enable you to find the flag in a single command: https://play.picoctf.org/practice/challenge/48
* Using your own computer, you could use qemu to boot from this disk!

## Solución
````
gzip -d dds*.gz
lesly@Lesly:~/anterior$ file *.img
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors
lesly@Lesly:~/anterior$ strings *.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_dcbf5942}
```
