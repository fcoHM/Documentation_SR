## Descripción 
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols. ssh -p 51943 ctf-player@mimas.picoctf.net Use password: 1ad5be0d
## Solución
esta terminal no reconoce lo comando basicos, se usa puro wilcards que son comandos que simplifican tareas ya se para buscar, manejar o econtar archivos al mismo timpo

- en este caso tenemos que encontar una traduccion de wilcards que signifique lo mismo que estoy buscando
- * : significa todos     /: direccion raiz      ?: se espera un valor ahi
- con esto podemos ir haciendo un propio listado de archivos que coincidan con el
- si metemos
```
*/*
```
nos arroga que en una carpeta blargth esta la flag.txt pero ocupamos saber donde esta es ruta por lo que hacemos lo siguiente

```
    */*

    /* <------ es la carepeta bien

    /*/??? <-----------esta es la carpeta /bin/awk

    /*/?????? <---------- /bin/base 64

    /*/???[!_]64 */* <---------------/bin/x86_64

    /*/???[!_]64 */????.* <------ esta es la carpeta donde esta la flag
```

cuando  hacemos uso de estos comando hace un espacie de cat pero wildcards 

- el ultimo nos devuelve un valor en base64
```
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV83NzVhYzEyZH0=

```

solucion:
```
picoCTF{7h15_mu171v3r53_15_m4dn355_775ac12d}
```