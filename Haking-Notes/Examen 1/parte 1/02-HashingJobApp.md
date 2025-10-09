## Descripción 
If you want to hash with the best, beat this test! nc saturn.picoctf.net 50122
## Solución
- en este caso la app pide que le pases textos que te da, pero encriptados con hash md5
- se fabrico un programa en python que usa la libreria haslib
```python
import hashlib
# Pedir entrada desde el teclado
texto = input("Ingresa el texto a hashear: ")
# Calcular el MD5
hash_md5 = hashlib.md5(texto.encode()).hexdigest()
# Mostrar el resultado
print(f"MD5 hash: {hash_md5}")
```
- se obtuvo el siguiente resultado
```bash
┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 50122
Please md5 hash the text between quotes, excluding the quotes: 'money'
Answer: 
9726255eec083aa56dc0449a21b33190
9726255eec083aa56dc0449a21b33190
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Michele Pfeifer'
Answer: 
5aa67b1e7680114db194886efc6967c2
5aa67b1e7680114db194886efc6967c2
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'cleaning the bathroom'
Answer: 
0c8acab58314dbcf54dbc158470a8047
0c8acab58314dbcf54dbc158470a8047
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_3eb82b73}
```


