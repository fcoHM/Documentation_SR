## Descripción 
Can you find the flag in file without running it?

## Solución
Bueno en este caso es exactamente lo mismo que el 15-Static ain't always noise, y va con la forma de la nota adicional
esta proponi usar el comando strings ya que este decodifica la  base en la que esta el archivo  y lo pasa a ASCII/UTF-8 pero esto no queda ahi, falta buscar la etiqueta pico y esto lo hacemos como ya lo hemos hecho con grep

```bash
strings strings | grep "pico"
```

dando como resultado

```
picoCTF{5tRIng5_1T_7f766a23}
```
## Notas adicionales

## Referencias

- https://labex.io/es/tutorials/linux-linux-strings-command-with-practical-examples-422934