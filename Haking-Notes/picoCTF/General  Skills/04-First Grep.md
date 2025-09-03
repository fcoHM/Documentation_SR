## Descripción 
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file)? This would be really tedious to look through manually, something tells me there is a better way.
## Solución
Se nos dio un archivo file, que en su interior, por lo cual entendemos que ahi tenemos que buscar la bandera, que en este caso se hizo un grep que buscara por palabras, que en nuestro caso era picoCTF que es el formato de la bandera a buscar

```bash
grep pico file
```

Lo cual se interpreta con que grep es un filtro y va a filtrar todo aquello que inicie con pico  y este en el archivo file, dando como resultado:

```
picoCTF{grep_is_good_to_find_things_5af9d829}
```

## Referencias
- contenido de repaso de linux en classroom
- apuntes de la clase de Sistema Operativo Linux