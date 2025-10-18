## Descripción 
Our server seems to be leaking pieces of a secret flag in its logs. The parts are scattered and sometimes repeated. Can you reconstruct the original flag?Download the [logs](https://challenge-files.picoctf.net/c_saffron_estate/5d7ef6ba5b43389856bbee30cb7c57ce54ec8c5f82c40ade5167994484fb0369/server.log) and figure out the full flag from the fragments.
## Solución
En este caso se nos proporciono un rachivo al cual si le hacemos un cat nos arroga muchos logs
por lo cual haremos 3 tipos de filtros

una flag de picoCTF se compone por las siguientes partes:

- apertura de la flag
```apertura
picoCTF{
```

- contenido: comunmente por guiones bajos
```contenido
contenido_contenido
```

- cierre de la flag:
```cierre
contenido}
```

Sabiendo las 3 partes de una flag haremos esos filtros

```bash
cat server.log|grep pico <--- buscar apertura
[1990-08-09 10:00:10] INFO FLAGPART: picoCTF{us3_


cat server.log|grep _   <--- buscar contenido de la flag
[1990-08-09 10:00:10] INFO FLAGPART: picoCTF{us3_
[1990-08-09 10:02:55] INFO FLAGPART: y0urlinux_
[1990-08-09 12:25:32] INFO FLAGPART: sk1lls_

cat server.log|grep "}" <----- cierre de la flag
[1990-08-09 10:10:54] INFO FLAGPART: cedfa5fb}
```

ya solo toca armar la flag con algo que tenga coherencia con la estructura:

```
picoCTF{us3_y0urlinux_sk1lls_cedfa5fb}
```


