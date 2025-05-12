- Filter your packets to narrow down your search.
- Attacks were done in timely manner.
- Time is essential

## Solución

[](https://github.com/JazSparrow/Hacking-notes-2025/blob/main/Hacking-notes-2025/PicoCTF/Tarea%203%20-%20Forensic/09_Ph4nt0m%201ntrud3r.md#soluci%C3%B3n)

Primero descargamos nuestro respectivo archivo y lo ubicamos en nuestra carpeta de linux.

Ingresamos a nuestra terminal de linux e ingresamos el siguiente comando para abrir el wireshark: wireshark myNetworkTraffic.pcap

Una vez dentro habrá 22 líneas y desde la primera iremos a la parte de Flags, y mas abajo nos aparece TPC payload (4 bytes) y Retransmited TCP segment data (4 bytes), iremos variando entre ambos y daremos clic derecho y seleccionamos Show Packet Bytes... una vez dentro nos aparecerá una decodificación en ASCII y la seleccionamos y la pegamos en el cyberchef entonces seleccionamos from base64 y nos ira transformando nuestra flag.

**NOTA IMPORTANTE: Cada flag es diferente, se debe buscar línea por línea hasta encontrar los TCP segment data, se puede cambiar para decodificar el ASCII a base64 directamente pero también se puede usar el cyberchef para una mejor referencia y orden en la bandera, como se observa en la siguiente imagen.**

file upz.png
picoCTF{fl4g_h45_fl4g1a2a9157}