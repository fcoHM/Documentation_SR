## Descripción 
We found this file. Recover the flag.
## Solución
encabezados dañados, no damos cuenta con hacerle un 
```bash
xxd mystery |head
```

- vemos que los chuncks nos a indicios de que es un png, pero hasta estos estan mal, y tambien la cabecera, por lo que tocara repararlos
- usaremos un editor de cabeceras para editarlo, esto con el formato que debe tener un png

| PNG | .png | 89 50 4E 47 0D 0A 1A 0A | Imagen PNG |
| --- | ---- | ----------------------- | ---------- |
```
headeditor mytery
```

- una vez puesto estos datos vemos que sigue siendo datos y no un png, asi que  toca arreglar los chunks
- vemos que el primer chunk no se llama como debe "IHDR" por lo que procedemos a cambiarlo con valores ASCII de las letras que este debe llevar 
  ```
  49 48 44 52
  ```

- ya es reconocido como png pero al abrirlo vemos que aun hay datos corruptos
- en este caso usaremos la siguinet herramienta para ver el estado de los archivos png
```bash
sudo apt install pngcheck
```

- usamos la herramienta para veer que problemas tiene
```
pngcheck -v mystery
```

- vemos que el problema viene del chunk phys, que es el que contiene la resoluciion de la imagen
- vemos que el tamaño de la imagen es muy grande
- asumiendo que es una imagen cuadrada procedemos a editar
```
00000042: 00 00 00 09 70 48 59 73 00 00 0B 13 00 00 0B 13  ....pHYs........
```

- revisamos de nuevo y vemos que tenemos problemas con 
## Notas adicionales
chunks: informacion despues del head que contiene informacion de la un archivo, comunmente se coforma de 4 partes, longitud de 4bytes, tipo de chunk en 4 bytes, chunk de informacion 4bytes y CRC de 4bytes esta ultima ayuda a corroborar que los datos tengan el tamaño correcto de los chunk, y en imagenes IHDR

el primer chunk despues del head es el mas critico

```
picoCTF{c0rrupt10n_1847995}
```
## Referencias
- fernunex


