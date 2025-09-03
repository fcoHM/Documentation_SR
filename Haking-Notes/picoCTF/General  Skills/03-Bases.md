## Descripción 
What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

## Solución
En este caso lo que se identifico es que el texto proporcionado esta en base 64, que en palabras de wikipedia:

"**Base64** es un conjunto de esquemas de codificación de binario a texto que transforma datos binarios en una secuencia de caracteres imprimibles, limitada a un conjunto de 64 caracteres únicos. Más específicamente, los datos binarios de origen se toman de 6 en 6 bits, y luego este grupo de 6 bits se asigna a uno de los 64 caracteres únicos."

Por lo cual para facilitar la traduccion se uso la pagina:
- https://www.base64decode.org/

Dando como resultado la siguiente bandera:
```
picoCTF{l3arn_th3_r0p35}
```
## Notas adicionales

## Referencias

- [[https://en.wikipedia.org/wiki/Base64]]