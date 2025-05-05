#### Description

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/01_MacroHard%20WeakEdge.md#description)

I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm]([https://mercury.picoctf.net/static/c00c449c3b08daaccacca6f9d5c55d49/Forensics](https://mercury.picoctf.net/static/c00c449c3b08daaccacca6f9d5c55d49/Forensics) is fun.pptm)

#### Hints

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/01_MacroHard%20WeakEdge.md#hints)

- (None)

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Forensic%203/01_MacroHard%20WeakEdge.md#soluci%C3%B3n)

Primero descargamos nuestro respectivo archivo y lo ubicamos en nuestra carpeta de linux, enseguida nos dirigimos a la terminal y entramos a las siguientes carpetas: `cd macro` `cd ppt` `cd slideMasters`

Y enseguida aplicamos los siguientes comandos para que nos convierta nuestro cifrado y nos muestre nuestra respectiva flag:

`cat hidden` `cat hidden | sed 's/ //'` `cat hidden | sed 's/ //g'` `cat hidden | sed 's/ //g' | base64 -d`

## Terminal de ejemplo:
````
 cd FSI/
cd macro
 ls
'[Content_Types].xml'   _rels   docProps   ppt
 cd ppt
ls
_rels          presentation.xml  slideMasters  tableStyles.xml  vbaProject.bin
presProps.xml  slideLayouts      slides        theme            viewProps.xml
 cd slideMasters
 cat hidden
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Qjazmin@DESKTOP-1CBQJ6D:~/FSI/macro/ppt/slideMasters$ cat hidden | sed 's/ //'
Zm x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f 

cat hidden | sed 's/ //g'

 cat hidden | sed 's/ //g' | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
```