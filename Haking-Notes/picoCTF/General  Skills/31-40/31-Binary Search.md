## Descripción 
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!

ssh -p 51692 ctf-player@atlas.picoctf.net
84b12bae
## Solución

Bueno en este caso, tuvimos que entrar por medio de ssh una maquina que autmaticamente lansa un programa, que si analizamos con el en el codigo propociondo es una reto de adivinar el numero dando pistas de si estas cercas o legos, por lo cual podemos utilizar la busqueda binaria, donde preguntamos por un numero intermedio, si este es mas grande o mas poco pdemos separar los elementos entre los mayores o menores y asi hasta llegar  al acertado.


```
┌──(kali㉿kali)-[~/Downloads/home/ctf-player/drop-in]
└─$ ssh -p 51692 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 600
Lower! Try again.
Enter your guess: 500
Lower! Try again.
Enter your guess: 400
Higher! Try again.
Enter your guess: 450
Lower! Try again.
Enter your guess: 425
Lower! Try again.
Enter your guess: 410
Lower! Try again.
Enter your guess: 405
Higher! Try again.
Enter your guess: 408
Congratulations! You guessed the correct number: 408
Here's your flag: picoCTF{g00d_gu355_2e90d29b}
Connection to atlas.picoctf.net closed.
```

aqui la respuesta:

```
picoCTF{g00d_gu355_2e90d29b}
```

