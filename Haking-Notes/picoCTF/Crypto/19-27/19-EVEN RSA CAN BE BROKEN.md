## Descripción 
This service provides you an encrypted flag. Can you decrypt it with just N & e? Connect to the program with netcat: `$ nc verbal-sleep.picoctf.net 63730` The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_verbal_sleep/68dea6cb63f53886d85611943a2abf0c22e38ce960966417f393cd053daee689/encrypt.py).
## Solución
- nos coencatamos al servidor
- nos da los siguientes datos:
```
N: 22928487515440259198206743552392399186329652286872162822865690163864949774727518557558348897915616650544874234300456386435151781612357996637187039937207978
e: 65537
cyphertext: 21587095822683893567879921175958758869117071184903032441636080885773320066958351074186236828890987525349455627178355015445053856692287601673252344367306973

```

- usamos rsa cipher 

solucion:
```
picoCTF{tw0_1$_pr!m3df98b648}
```

## Notas adicionales

# Referencias
- https://www.dcode.fr/rsa-cipher