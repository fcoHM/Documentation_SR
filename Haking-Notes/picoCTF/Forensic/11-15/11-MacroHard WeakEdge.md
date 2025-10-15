## Descripción 
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/c0da20f29337e87ffb58ea987d8c596e/Forensics%20is%20fun.pptm)
## Solución
- se no sproporciono una archivo
- revisamos el archivo con file 
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ file 'Forensics is fun.pptm' 
Forensics is fun.pptm: Microsoft PowerPoint 2007+
```

 - vemos que es un archivo de power point del 2007 
 - des-empaquetamos el archivo .pptm
 - vemos que no funciona el filtrado de archivos
 - hacemos una busqueda manual para encontrar la flag usando tree, que nos muestra un arbol de la estructura de las carpetas, vemos unas que se llama hidden
 - entramos en la carpeta y vemos quie tiene una archivo, que tiene una cadena en basde 64
 ```
 Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q
 ```

- decodificamos la cadena 
```
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```
## Notas adicionales
 - los archivos .pptm, es una esacie de empaquetado, por lo cual podemos des empaquetarlo y ver contenido a contenido del archivo, y podmeos ver que tiene una estructura xml muy interensante
## Referencias

- https://www.youtube.com/watch?v=CsCeOp9PFGs&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=28
