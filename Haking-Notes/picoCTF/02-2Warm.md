## Descripción 
Can you convert the number 42 (base 10) to binary (base 2)?

## Solución
Para solucionar el prblema lo que tenemos que hacer es tener en cuenta que tenemos que agarrar los valores que sumados den 42.

| Potencia | Expresión | Valor |
| -------- | --------- | ----- |
| 2⁰       | 2^0       | 1     |
| 2¹       | 2^1       | 2     |
| 2²       | 2^2       | 4     |
| 2³       | 2^3       | 8     |
| 2⁴       | 2^4       | 16    |
| 2⁵       | 2^5       | 32    |
| 2⁶       | 2^6       | 64    |
Como podemos ver en la anterior tabla  se ven los valores, en este caso **solo escogere aquellos que sumados me den 42**, que en este caso serian: **32, 8, 2**  y aqullos que no utilice serian 0 y lo que si utilice serian 1
quedando como resultado: 101010

```
picoCTF{101010}
```
## Notas adicionales

Tambien se puede hacer dividiendo entre 2
- **Cuando el número es par**, el residuo es **0** → ese 0 se agrega al resultado.
- **Cuando el número es impar**, el residuo es **1** → ese 1 se agrega al resultado.

| División | Cociente | Residuo |
|----------|----------|---------|
| 42 ÷ 2  | 21       | 0       |
| 21 ÷ 2  | 10       | 1       |
| 10 ÷ 2  | 5        | 0       |
| 5 ÷ 2   | 2        | 1       |
| 2 ÷ 2   | 1        | 0       |
| 1 ÷ 2   | 0        | 1       |
El resultado es el mismo: 101010

## Referencias

- [[https://www.youtube.com/watch?v=QqVcxYR8Zb8]]
