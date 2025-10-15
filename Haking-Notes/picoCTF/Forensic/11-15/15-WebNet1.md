## Descripción 
We found this packet capture and key. Recover the flag.
## Solución
- se nos proporciono un archivo .pcap 
- se nos proporciono una llave RSA
- cargamos la llave RSA para desencrptar el flujo de datos https
- de los paquetes desencriptado podemos ver que el paquete 47 hay una descarga de una imagen
- extraemos el objeto con export objects 
 ![[Pasted image 20251014222449.png]]

- procedemos a revisar la imagen
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ grep -a pico vulture.jpg     
����JFIF���ExifMM▒J(;ZpicoCTF{honey.roasted.peanuts}��ICC_PROFILE
lcmsmntrRGB XYZ �)9acspAPPL���-lcms
```

solucion:
```
picoCTF{honey.roasted.peanuts}
```
## Notas adicionales

## Referencias

- https://www.youtube.com/watch?v=Ym3i79nEHjw&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=25
