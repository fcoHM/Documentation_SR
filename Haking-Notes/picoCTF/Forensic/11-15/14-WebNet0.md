## Descripción 
We found this packet capture and key. Recover the flag.
## Solución
- se nos proporciono un archivo .pcap
- tambien se nos proporciono la llave de encriptacion de los datos
- abrimos la captura de paquetes con wiresharck
- vemos que tenemos una trasmicion de tls
- segmos la trasmicion
- en wiresharck cargamos la llave RSA
- hacemos una busqueda en los detalles de los paquetes, buscamos una cadena picoCTF

obtenemos lo siguiente:
```
[Pico-Flag: picoCTF{nongshim.shrimp.crackers}\r\n
```

```
picoCTF{nongshim.shrimp.crackers}
```
## Notas adicionales
TLS: transport  layer security es un portocolo de encryptacion  diseñado para proveer comunicasiones seguras sobre una red de computadora
usa varias certifacasiones de seguridad, se usa muy frecuentemente en estructuras cliente servidor, donde se espera tener una llave por ambos lados para decifrar el contenido usando metodos asimetricos

- se pudo resolver buscando simplemente despues de desencriptar
- tambien se puso resolver de la siguiente manera
```bash
ssldump -r capture.pcap -k picopico.key -d |grep pico -A 2
```
## Referencias


