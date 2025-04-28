#### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
#### Hints 

(None)

## solución
````
wget https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap

			si no lo  tienes sudo apt install wireshark


wireshark capture.pcap & 

busca el paquete start - filtra los puertos destino 22

from scapy.all import *


creas un pyton "exp.py"

----------------------------------------------------------
packets =rdpcap('capture.pcap')
flag = ''

for p in packets:
        if UDP in p and p[UDP].dport=22:
                if p[UDP].sport > 5000:
                        flag += chr(p[UDP].sport - 5000)
print(flag)

--------------------------------------------------------------

python exp.py 

```