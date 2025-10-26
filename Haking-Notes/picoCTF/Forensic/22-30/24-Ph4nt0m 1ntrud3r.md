## Descripción 
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag. To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder! Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/3fe089c41615b9413666bedca922e07bf6ad8894a3dabd2737735143ad2396cf/myNetworkTraffic.pcap) and try to get the flag.
## Solución
- se nos proporciona un pcap, que como sabemos es una captura de paquetes viajados por la red
- vemos que la mayoria de los paquetes pesan 8 bytes mientras unos pocos pensan 12 y da la casualidad de tener como carga util valores en base 64
- tratamos de decodificar la flag atravez de estos paqutes
- los ordenamos en base al tiempo y tenemos lo siguiente
```
picoCTF
{1t_w4s
nt_th4t
_34sy_t
bh_4r_9
66d0bfb}
```

y esto es la solucion
```
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_966d0bfb}
```


