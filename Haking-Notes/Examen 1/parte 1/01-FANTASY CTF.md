## Descripción 
Play this short game to get familiar with terminal applications and some of the most important rules in scope for picoCTF. Connect to the program with netcat: $ nc verbal-sleep.picoctf.net 53790
## Solución
- entramos desde la terminal al servidor que nos dan
- vemos que es un juego donde tenemos que ir avanzando y buscando en la las opciones del juego
```
Options:
A) *Register multiple accounts*
B) *Share an account with a friend*
C) *Register a single, private account*
[a/b/c] > c   
```

- escogemos la opcion "c" que despuede segir una larga conversacion nos pide lo siguiente
```
Options:
A) *Play the game*
B) *Search the Ether for the flag*
[a/b] > a
```

- escogemos las opcion "a" que lo que haces es simular la descarga de un archivo y continia la platica hasta que da lo siguiente
  ```
  "Thanks, Nyx! Here's the flag I found: picoCTF{m1113n1um_3d1710n_f71e4e49}"
  ```


