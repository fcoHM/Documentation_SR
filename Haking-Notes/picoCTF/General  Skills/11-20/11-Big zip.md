## Descripción 
Unzip this archive and find the flag.
		Donwload zip file
## Solución
Para este caso lo que se hizo fue descomprimir el .zip usando el comando unzip

```bash
unzip big-zip-files
```

para despues usar el comando grep buscando la palabra pico o similares, esto usando la funcion r que esto indica  que sera de manera recursiva en un directorio 

```bash
grep -r "pico" /big-zip-files/
```

resultado:
```
picoCTF{gr3p_15_m4g1c_ef8790dc}

```
## Notas adicionales

## Referencias

- comando mandado a classroom y ayuda de las pistas 
