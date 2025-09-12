## Descripción 
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 35652`, but it doesn't speak English...
## Solución
En esta caso me percate que los valores arrogados por la terminal eran valores en ANCII por lo cual me dispuse hacer un pequeño script usando la funcion chr() que biene por default en python, la cual si le pasas un valor en ACII decodifica su valor y te regresa su valor en caracter.

```Python
valores = [ #valores iniciales
    112, 105, 99, 111, 67, 84, 70, 123, 103, 48, 48, 100, 95, 107, 49, 116,
    116, 121, 33, 95, 110, 49, 99, 51, 95, 107, 49, 116, 116, 121, 33, 95,
    57, 98, 51, 98, 55, 51, 57, 50, 125, 10
]

flag = "" # bandera
for i in range (len(valores)):
    valor = chr(valores[i]) # decode de los valores
    flag += valor # bandera resultado

print(flag) # mostrar resultado 
```
## Notas adicionales

## Referencias

- https://www.python.org/doc/essays/list2str/