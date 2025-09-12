## Descripción 
Our flag printing service has started glitching!
Additional details will be available after launching your challenge instance.
## Solución
en este caso lo que se debe hacer es iniciar la maquina, y esta nos da una bandera corrupta, la cual nos da valores en hexadecimal y pero la funcion esta mal y te da las funciones de des-encriptar en un cadena en vez de ejecutar la funcion 

```
llave corrupta:
picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
```

Aqui podemos ver que los valores que estan en  chr(), son los que tenemos que decifrar, por lo cual nostros le quitaremos las comillas y se lo pasaremos a python]

```Python3
picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}
```

Resultado:
```
picoCTF{gl17ch_m3_n07_bda68f75}
```
## Notas adicionales

The chr() function returns the character that represents the specified unicode.
## Referencias

- https://www.w3schools.com/python/ref_func_chr.asp