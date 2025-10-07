## Descripción 
There's something in the building. Can you retrieve the flag?
## Solución
se nos entrego un archivo png que solo tiene una imagen del archivo

- si usamos una pagina que nos diga que hay oculto en el archivo no arroga lo siguiente
- primero revisa el tipo de archivo
- luego revisa que tipo de encriptacion se uso

```
picoCTF{h1d1ng_1n_th3_b1t5}
```


- si usamos la terminal
- metemos el siguiente comando para instralar la herramienta
```bash
sudo gem install zsteg
```

esta herramienta tambien detecta la tecnica utilizada y trata de decodificar
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ zsteg -a buildings.png | grep pico
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"

```
## Notas adicionales

Que es estenografia?
	implica ocultar informacion sensitiva en un archivo ordinario no secreto, para no ser detectado, muy usado para ocultar informacion, puede ser en cualquier topo se archivo
	
	
## Referencias

- https://www.youtube.com/watch?v=bFUB-USG3sw&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=18
