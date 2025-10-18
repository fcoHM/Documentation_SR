## Descripción 
We’re in the middle of an investigation. One of our persons of interest, ctf player, is believed to be hiding sensitive data inside a restricted web portal. We’ve uncovered the email address he uses to log in: ctf-player@picoctf.org. Unfortunately, we don’t know the password, and the usual guessing techniques haven’t worked. But something feels off... it’s almost like the developer left a secret way in. Can you figure it out?

## Solución
En este caso se nos idica que el siguiente correo no se sabe su contraseña, por que esta escriptada

- lo primero que hacemos es revisar el codigo funente de la web
- en este encontraremos un comentario que aparentemente esta encryptado

```
ABGR: Wnpx - grzcbenel olcnff: hfr urnqre "K-Qri-Npprff: lrf" 
```

siguiendo la pista sabemos que esta escriptado en 13 posiciones que esto cruadra con el metodo de "encriptacion de cesar", por lo que podemos meterlo a la en encoder y que lo rote 13 veces las posiciones, dando como resultado

```
NOTE: Jack - temporary bypass: use header "X-Dev-Access: yes"
```

viendo que es una encabezado, lo que haremos es capturar el metodo post con el cual se manda a llamar el metodo que verifica la contraseña, y en burpsuite lo mandamos a repeater, ahi agregamos la cabecera y hacemos un request, dando como resultado:

```
picoCTF{brut4_f0rc4_7e5db33b}
```


