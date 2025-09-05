## Descripción 
Can you look at the data in this binary: static? This BASH script might help!
## Solución
bueno en este caso se nos esta dando un archivo  llamado static, este le hacemos un cat nos da unos caracteres raros

```
8#TT 1tt$D���o�N[~]
�� � @ @ �0@)▒  p�▒V``�^y▒�  
```

asi que toco revisar el el binario del archivo para ver que podemos encontrar, por lo cual hacemos un escaneo forzado con grep -a

```bash
grep -a "pico" static
```

donde -a trata al binario como si fuera texto, dando como resultado 

```
 picoCTF{d15a5m_t34s3r_1e6a7731}GCC: (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.08Tt��`�
```
## Notas adicionales

tambien se puede hacer con un funcion llamada strings 

```bash
grep -a "pico" static
```

la diferenacia es que esta funcion extrae todo en ASCII/UTF-8 de un binario y se lo manda a grep para buscar la palabra especificada 
## Referencias

-  https://es.stackoverflow.com/questions/855/c%C3%B3mo-convertir-un-archivo-binario-a-ascii-en-unix
- https://labex.io/es/tutorials/linux-linux-strings-command-with-practical-examples-422934 