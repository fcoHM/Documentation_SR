## Descripción 
Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?
## Solución
- se nos dio 3 archivos, flag.txt.en, ende.py y pw.txt
- se probo ejecutar el archivo .py
- nos regreso esto
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ python ende.py                                              
Usage: ende.py (-e/-d) [file]
```

lo cual nos indica que debemos usar las dunciones -d o -e
- -d     Turn on parser debugging output (for expert only, depending on compilation options).
- la funcion -e no existe en python
ya con esto podmeo smnadarle el archivo flag.txt,pero primero veamos lo contenidos
```bash
──(kali㉿kali)-[~/Downloads]
└─$ cat flag.txt.en 
gAAAAABgUAIVX7N_dNxY0j5lWtsDEN2b-h0mN-Lyhm_9QaEdwFK4em1kGiAV52ewbKv8wZJL2QwecZ7kTsVQ11PYEL3BJLD4LVyKrCKAvTFu5-1yuNGFAXKBY8GO3nIReXuOUbaSwVHl                                                    

┌──(kali㉿kali)-[~/Downloads]
└─$ cat pw.txt      
192ee2db192ee2db192ee2db192ee2db
```

- parentemente no hay nada raro asi que procedemos mandando el archivo y usando la contraseña
  
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ python ende.py -d flag.txt.en 
Please enter the password:192ee2db192ee2db192ee2db192ee2db
picoCTF{4p0110_1n_7h3_h0us3_192ee2db}
```


solucion:
```
picoCTF{4p0110_1n_7h3_h0us3_192ee2db}
```


