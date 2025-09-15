## Descripción 
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:
## Solución
Bueno descargando y descomprimiendo nos damos cuenta que contiene versionado de arhivos con git, por lo cual podemos decir que hay un historial de commits 

lo primero que vamos a hacer es contar cuentas lineas hay para tener nocion de por donde buscar 

```bash
git log | wc -l
2993
```

lo que hace este comando es contar la lineas de git log, de lo cual unicamente nos interesan las ultimas, por lo cual ponemos lo siguinete 

```bash
git log | tail -50
```
lo que haces agarrar de git log las ultimas 50 lineas y mostrarlas en pantalla, y en un de ellas nos podemos percatar que un autor tiene de nombre la flag

```
commit 8c83358c32daee3f8b597d2b853c1d1966b23f0a
Author: picoCTF{@sk_th3_1nt3rn_2c6bf174} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:11 2024 +0000

    optimize file size of prod code
```


## Referencias

- documentacion de git