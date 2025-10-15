## Descripción 
We found this file. Recover the flag.
## Solución
- se nos proporciona un archivo de tipo bitmap con xxd 
- vemos que esta algo ofuscado
- le agregamos la extencion de .bmp
- si se trata de abrir vemos que no hay nada 
- editamos el archivo en la posicion 0x0E que debe ser 28 que es el valor en hexadecimal que representa los 40 bits
- nos desplazamos a la posicion 0x0A que vemos que tambien esta mal, corregimos con 28 paea que cargen los datos de la imagen 
- vemos que ya se puede abrir la imagen pero no no hay nada 
![[noflag.png]]

- usamos exiftool para ver metadatos, vemos que la imagen esta limitada en lo alto, vamos a tratar de hacerla un poco mas alta pa ver si logramos encontrar algo 
- el ancho esta en 0x12 y en el 0x16 esta el alto
- lo modificamos con un 40 para ver si cambia el alto
- vemos que si se expandio poco, asi que le aumentamos un poco ams

solucion:
```
picoCTF{qu1t3_a_v13w_2020}
```
## Notas adicionales
formato de archivo de imagen "bitmap" (mapa de bits), que se utiliza para imágenes digitales de alta calidad pero de gran tamaño, el encabezado cambie dependiendo del sistema en el que fue creado en este caso fue echo en windows
## Referencias

 - https://www.youtube.com/watch?v=1ucy2G1PIh4&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=27&t=84s
