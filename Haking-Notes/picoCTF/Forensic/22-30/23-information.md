## Descripción 
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/7cf6a33f90deeeac5c73407a1bdc99b6/cat.jpg)
## Solución
- se nos proporciono una imagen
- se reviso el contenido y no habia la gran cosa
- revisando los metadatos con exiftool, se hayo un campo **licenia** que tenia lo siguiente que parece ser base 64
```
cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
```

- si decodificamos encontramos lo siguiente
```
picoCTF{the_m3tadata_1s_modified}
```


