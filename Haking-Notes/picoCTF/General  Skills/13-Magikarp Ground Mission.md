## Descripción 
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `a13b7f9d`

Additional details will be available after launching your challenge instance.
## Solución

en este caso nos tuvimos que conectar por ssh a una maquina remota la cual nos da un usuario y constraseña 

```
`ctf-player` with the password, `a13b7f9d`
```

para conectarnos usamos el comando
```bash
ssh ctf-player@venus.picoctf.net -p 55480
```

donde espcificamos a donde y con que puerto nos conectaremos, nos pedira la contraseña  ya mencionada y con esta estaremos adentro


en este caso nos pusimos a explorar  y encontramos archivos llamados flag y archivos instructions, por lo cual nos ponemos a consultarlos con cat dando el siguiente flujo



```bash
cat 1of3.flag.txt 
picoCTF{xxsh_
cat instructions-to-2of3.txt
Next, go to the root of all things, more succinctly `/`
cd /
ls
2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run 
cat 2of3.flag.txt
0ut_0f_\/\/4t3r_ 
cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
cd ~
ls
3of3.flag.txt  drop-in
cat 3of3.flag.txt
71be5264}

```

dando como resultado

```
picoCTF{xxsh_0ut_0f_\/\/4t3r_71be5264}

```
## Notas adicionales

## Referencias

- apuntes viejos de la clase de Sitema operativo linux y comandos mandados a classroom