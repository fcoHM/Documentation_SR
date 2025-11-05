## Descripción 
We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/129/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solución
- se nos da un archivo .txt el cual contiene la siguiente informacion
```
350 63 353 198 114 369 346 184 202 322 94 235 114 110 185 188 225 212 366 374 261 213
```

- usamos el siguinete script para obtener la flag 
```python
numbers = [350, 63, 353, 198, 114, 369, 346, 184, 202, 322, 94, 235, 114, 110, 185, 188, 225, 212, 366, 374, 261, 213]
flag = ""
for n in numbers:
	c = int(n) % 37
	if c >= 0 and c <= 25:
		s = chr(c+65)
	elif c >= 26 and c <= 35:
		s = chr(c+22)
	else:
		s = '_'

flag += s

print(flag)
R0UND_N_R0UND_ADD17EC2
```


solucion:
```
picoCTF{R0UND_N_R0UND_ADD17EC2}
```
## Notas adicionales

# Referencias
