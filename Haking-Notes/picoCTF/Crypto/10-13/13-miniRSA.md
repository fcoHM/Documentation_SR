## Descripción 
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/ee7e2388b45f521b285334abb5a63771/ciphertext)? Something seems a bit small.
## Solución
- se revisa los dadtos en el archivo dado
-  vemoss que tenemos una 'e=3' muy pequeña, por lo vamos a uar un vulnerabilidad de raiz cubica
```
c = m^3
```
- se uso s1.py: modificado en el mensaje

modificasion:
```
c = 2205316413931134031074603746928247799030155221252519872649649212867614751848436763801274360463406171277838056821437115883619169702963504606017565783537203207707757768473109845162808575425972525116337319108047893250549462147185741761825125
```  

resultados
```
b'picoCTF{n33d_a_lArg3r_e_606ce004}'
```

## Notas adicionales
tambien sse puede ussar la s3.py
## Referencias
- video clasroom