## Descripción 
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext).
## Solución
- revisamos el archivo con cat, y nos regresa lo siguiente
```
picoCTF{dspttjohuifsvcjdpoabrkttds}
```

- pareciera estar caso bien, por lo que nos enfocamos en l a parte interna
- vemos que parec rot13, asi que lo deciframos
```
crossingtherubiconzaqjsscr
```
- vemos que esta resultado parece coherente, lo probamos en la flag y vemos que funciona 
- solucion
```
picoCTF{crossingtherubiconzaqjsscr}
```



