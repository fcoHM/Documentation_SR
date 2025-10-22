## Descripción 
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/2/enc_flag).
## Solución
- revisamos el archivo que se nos da y vemos que parece basse64
```bash
cat enc_flag 
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6YzRNalV3YUcxcWZRPT0nCg==
```
- tratamos de ver si en base64 dice algo y vemos al muy curioso en la inscripcion d
```bash
base64 -d enc_flag 
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzc4MjUwaG1qfQ=='
```

- nos devuelve una cadena que pareciera estar en base 64 tambien, pero en este caso se la pasaremos a un decoder de base 64 ya que el decoder de la terminal solo funciona para archivos dando el sifuiente resultado
```
wpjvJAM{jhlzhy_k3jy9wa3k_78250hmj}
```

- y vemos que este pareciera estar encriptado en rot13
```
picoCTF{caesar_d3cr9pt3d_78250afc}
```
## Notas adicionales

## Referencias

- https://www.base64decode.org/
- https://www.dcode.fr/cifrado-cesar
