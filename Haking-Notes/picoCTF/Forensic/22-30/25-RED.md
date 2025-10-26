## Descripción 
RED, RED, RED, RED Download the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)
## Solución
- se nos da una imagen la cual es una imagen totalmente  roja 
- si revisamos las lines legibles de la imagen vemos que hay un poema, 
- si revisamos lo metadatos y vemos que la imagen es rgb y contiene el alfa
- con zsteg podemos revisar ese canal 
```
┌─[✗]─[francisco@parrot]─[~/Downloads]
└──╼ $sudo zsteg --lsb --channel rgba red.png 
b1,rgba,lsb,xy      .. text: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="
b2,rgba,lsb,xy      .. file: OpenPGP Secret Key

```

- y nos da una cadena que parece estar en base 64, decodificamos y nos da lo siguiente
```
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}65Dg#6E5F5VCGC57W#5c%SFF3SUpicoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}65Dg#6E5F5VCGC57W#5c%SFF3SU
```


- solucion
```
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}
```
## Notas adicionales

## Referencias


