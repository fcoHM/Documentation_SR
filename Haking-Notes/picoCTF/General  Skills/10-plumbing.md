## Descripción 

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.

## Solución

En este caso se hizo una convinacion entre comando que en este caso fue netcat, el pipel y grep

```bash
nc jupiter.challenges.picoctf.org 4427 | grep pico
```

que en este caso lo que hace es conectarse a la siguiente direccion y la respuesta se lo mandamos con un pipe " | " a grep que con este aplicamos un filtro que busque  las lineas que tenga la palabra pico, dando la siguiente bandera.

```
icoCTF{digital_plumb3r_5ea1fbd7}

```

## Notas adicionales

## Referencias

-  Ejercisios First Grep, Nice NetCat y comandos basicos mandados en classroom