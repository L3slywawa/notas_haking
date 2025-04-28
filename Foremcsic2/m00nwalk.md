#### Description

Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.
#### Hints 

* How did pictures from the moon landing get sent back to Earth?
* What is the CMU mascot?, that might help select a RX option

## solucion
 
 ```
 cd /opt
 sudo ```
git clone https://github.com/colaclanth/sstv.git


sstv -d message.wav -o flag.png

cd sstv 

sudo python setup.py install

sstv -d message.wav -o flag.ong

open flag.png

```
 