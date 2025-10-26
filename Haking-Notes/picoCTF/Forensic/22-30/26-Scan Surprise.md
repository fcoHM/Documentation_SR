## Descripción 
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead? You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/2/challenge.zip)

The same files are accessible via SSH here: `ssh -p 62015 ctf-player@atlas.picoctf.net` Using the password `1ad5be0d`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
## Solución
- se nos da el codigo que esta montado en el server
- nos conectamos y vemos que hay nos da un qr y abre una terminal donde podemos ver una imagen de qr
- viendo lo montado vemos que es lo mismo que vemos 
- escaneamos el qr y el encabezado es la flag

![[scan.jpg]]

- solucion 
```
picoCTF{p33k_@_b00_b5ce2572}
```

