## Descripción 
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://artifacts.picoctf.net/c/151/leak.tar). The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.****
## Solución
- se nos da un archivo .tar que tiene un archvio de contraseñas y otro de usarios
- buscamos la posicion de cultiris y vemos que es la 378, asi que nos traemos el registro de la contraseña en esa misma posicion

```
password:cvpbPGS{P7e1S_54I35_71Z3}
user:cultiris
```

vemos que la contraseña es algo curiosa, pareciera ser root 13, asi que probamos 

solucion:
```
picoCTF{C7r1F_54V35_71M3}
```
## Notas adicionales

# Referencias
