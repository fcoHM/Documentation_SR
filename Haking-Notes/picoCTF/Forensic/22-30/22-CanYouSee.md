## Descripción 
How about some hide and seek? Download this file [here](https://artifacts.picoctf.net/c_titan/129/unknown.zip).
## Solución
- se nos proporciona un a imagen comprimida
- la descomprimimos y vemos que no tiene nada sospechoso al abrirla y al revisar el contenido
- revisamos los metadatos con exiftool
- vemoss que hay un campo URL con una cadena que parece sewr base 64
```
cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg==
```
- le decodificamos y obtenemos la siguiente flag
```
picoCTF{ME74D47A_HIDD3N_b32040b8}
```



