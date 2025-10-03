## Descripción 
We found this packet capture. Recover the flag.
## Solución
que es captura de paquetes??
- pcap es una API que nos permite capturar trafico vivo de la red que van viajando de la capa 2 a 7 del modelo OSI, se puede usar unalizador de red como wireshark para crear un archivo .pcap donde se guarda los datos de la red , comunmente tiene la forma WinPcap, Libpcap y PCAPng, pero comunemnte es para ver la informacion mandada en protocolos TCP/IP y UDP
- cuando usar pcap:
	cuando se quiere tener un registro  de analisis y monitoreo del trafico de la red 

- se metio el archivo a wireshark y se agarro un archivo UDP random y se le dio seguimiento, hasta hayar la flag
```
picoCTF{StaT31355_636f6e6e}
```
## Notas adicionales

que es wireshark?
	Wireshark is a GUI network protocol analyzer. It lets you interactively browse packet data from a live network or from a previously saved capture file. Wireshark's native capture file formats are pcapng format and pcap format; it can read and write both formats.. pcap format is also the format used by tcpdump and various other tools; tcpdump, when using newer versions of the libpcap library, can also read some pcapng files, and, on newer versions of macOS, can read all pcapng files and can write them as well.

## Referencias


