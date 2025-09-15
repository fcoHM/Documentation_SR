## Descripción 
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together? You can download the challenge files here:

## Solución
En este caso lo que nos damos cuenta tambien, es de que se trata de una archivo versionado, por lo cual podemos intuir que la flag esta escondida en algun commit, en este caso al hablar de colaborativo, una practica muy usal es que cada quien lleves su trabajo por separado por lo cual podemos decir que va ahaber ramas de git en las que podemos investigar


```bash
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
```

aqui ya podemos ver que hay 3 ramas para poder investigar


por lo cual procedemos a ver el rastro

```bash                       
       
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git checkout feature/part-1
Switched to branch 'feature/part-1'

┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ cat flag.py                
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')                                                                              
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git checkout feature/part-2
Switched to branch 'feature/part-2'

┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ cat flag.py                
print("Printing the flag...")
print("m@k3s_th3_dr3@m_", end='')                                                                                
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git checkout feature/part-3
Switched to branch 'feature/part-3'
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ cat flag.py                
print("Printing the flag...")
print("w0rk_7ffa0077}")
```

por lo cual la flag es:
```
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ffa0077}
```


## Notas adicionales

## Referencias

- documentacion de git