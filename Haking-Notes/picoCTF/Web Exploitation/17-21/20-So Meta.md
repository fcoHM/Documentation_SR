## Descripción 
Find the flag in this picture.
## Solución
- se reviso el archivo con cat
```bash
cat image_pico.png
```

- en esta encontramos la siguiente flag
  ```
  picoCTF{s0_m3ta_fec06741}
  ```
## Notas adicionales

Que son los metadatos:
- son datos que describen otros datos pero no el contenido de los datos, como el texto de una imagen
Tipos de metadatos:
- Descriptivos:
	Para encontrar o entender una fuente de información.
- Administrativos: 
	Metadatos técnicos: Para decodificar y representar archivos. - Metadatos de preservación: Gestión a largo plazo de archivos. - Metadatos de derechos: Derechos de propiedad intelectual adjuntos al contenido.
- Estructurales: 
	Relaciones de partes de recursos entre sí.
- Lenguajes de marcado: 
	Integra metadatos y marcas para otras características estructurales o semánticas dentro del contenido 


- Ta,bien se puede resolver con exiftool
	```bash
	exiftool pico_img.png
	```
## Referencias

- https://www.youtube.com/watch?v=Govu_p-wf4I&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=15
