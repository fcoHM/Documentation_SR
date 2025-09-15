## Descripción 
How well can you perfom basic binary operations?
Additional details will be available after launching your challenge instance.

nc titan.picoctf.net 63331
## Solución
En este caso tenemos que resolver las operaciones  que se piden, que ente caso son operaciones de numeros binarios, donde  la utima respuesta debera ser pasada a hexadecimal.

```
Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01110100
Binary Number 2: 01000111


Question 1/6:
Operation 1: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10111011
Correct!

Question 2/6:
Operation 2: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01000100
Correct!

Question 3/6:
Operation 3: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10000000101100
Correct!

Question 4/6:
Operation 4: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 00100011
Correct!

Question 5/6:
Operation 5: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 10001110
Incorrect. Try again
Enter the binary result: 011101000
Correct!

Question 6/6:
Operation 6: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01110111
Correct!

Enter the results of the last operation in hexadecimal: 77

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_675602ae}  
```

solucion:
```
picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_675602ae}
```
## Notas adicionales

## Referencias

- Practica de estructuras de datos: manejo de imagenes
- https://github.com/fcoHM/Estructura-Datos/blob/main/Analisi-practicas/practica_8_ED.pdf