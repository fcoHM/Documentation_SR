## Descripción 
We found this packet capture. Recover the flag that was pilfered from the network.
## Solución
se nos da un archivo .pcap, que como ya habiamos visto es una captura de paquetes

- tomamos un paquete UDP
- le seguemos el rastro para buscar indicios de una flag
```
icoCTF{StaT31355e
```
- se econtro este fragamento
- mas adelante se encontro un paquete con la palabra start, que  va del puerto 5000 al 22 con una longuitud de 5
- en el paquete 60 encontramos la palabra end, esto nos y comparte tambien con destino al 22
- filtramos por puerto 
```
udp.dstport == 22
```

- pero vemos que hay un patro de que si vamos viendo todos lo puesrto salen del 5000 pero variando, y si les vamos restando 5000 nos va dando  valores que podemos meter en la funcion chr() de python y asi decifrar la flag
- hacemos un script, usando scapy

```python
from scapy.all import *
pack = rdpcap("capture.pcap")
flag = ""
for p in pack:
	 if UDP in p and p[UDP].dport ==22: # solo los detino 22
		if  p[UDP].sport >5000:
			flag ++ chr(p[UDP].sport-5000)
			
print(flag)
```

```
picoCTF{p1LLf3r3d_data_v1a_st3g0}
```
## Notas adicionales
- se le puede mandar la IA para que haga el proceso de sacado de la flag 
## Referencias


