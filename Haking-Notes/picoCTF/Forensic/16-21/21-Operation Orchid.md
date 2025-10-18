## Descripción 
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/213/disk.flag.img.gz)
## Solución
- gzip al archivo .img que nos dan 
- con mmls vemos las particiones de la imagen y vemos que hay 3 de linux 
- con fls -o vamos viendo el contenido listado de la .img
		- 2048 
		- 206848 <-- esta no esta definida por el system
		- 411648
- en esta ultima vemos que esta root, entramos
- vemos que esta flag.txt.enc, lo cual nos dice que esta encriptado

```bash
1. Buscar referencias a "pico"
strings -t d disk.flag.img | grep pico
- strings: Extrae texto legible de archivos binarios
- -t d: Muestra offsets en formato decimal  
- grep pico: Filtra líneas que contienen "pico"
- Función: Buscar referencias relacionadas con "pico" en la imagen de disco

2. Buscar referencias a "flag.txt"
strings -t d disk.flag.img | grep flag.txt
- Busca todas las apariciones de "flag.txt" en la imagen de disco
- Revela que el archivo fue encriptado y luego eliminado con shred
- Muestra el comando OpenSSL usado para encriptar

3. Extraer archivo encriptado
icat -o 411648 disk.flag.img 1782 > flag.txt.enc
- icat: Herramienta de The Sleuth Kit para exportar archivos
- -o 411648: Offset del sistema de archivos (en sectores)
- 1782: Nodo del archivo a recuperar
- > flag.txt.enc: Redirige la salida al archivo flag.txt.enc
- Función: Extrae el archivo encriptado de la imagen de disco

Resumen del proceso:
- Se analizó la imagen de disco buscando pistas con strings
- Se identificó que flag.txt fue encriptado con OpenSSL AES256
- Se recuperó el archivo flag.txt.enc usando icat para posterior descifrado
```

solucion 
```
picoCTF{h4un71ng_p457_5113beab}
```
## Notas adicionales

## Referencias
- https://www.youtube.com/watch?v=fxFSrynEb9E

