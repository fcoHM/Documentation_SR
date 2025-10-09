## Descripción 
There's a flag shop selling stuff, can you buy a flag? Source. Connect with nc jupiter.challenges.picoctf.org 44566.
## Solución
- se nos proporciono el codigo que dice como se maneja el programa
- a parecer no se hace una validacion correcta del valance del dinero
- compramo una "thats is a not flag flag" y ponemos que queremos una cantidad muy grande ejemplo 2500000000000
- esto hara que nuestro valance quede en nagativo, con esto tratamos de comprar una 1337 flag, ya que esta vale bastante, pero como nstros nuestro balance es menor, nos pide una moneda, por que la damos y por la pesima validacion que vuelve a multiplicar el valor por si mismo obtenemos lo soguiente
```
picoCTF{m0n3y_bag5_68d16363}
```

