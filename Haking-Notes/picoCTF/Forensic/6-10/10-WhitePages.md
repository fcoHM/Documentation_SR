## Descripción 
I stopped using YellowPages and moved onto WhitePages... but the page they gave me is all blank!
## Solución
si usamos cat se muestra trasparente
- vemos que puede estar en unicode con un esquema UTF-8 esto lo vemos con el comando file 
```bash
file whitepages.txt
whitepages.txt: Unicode text, UTF-8 text, with very long lines (1376), with no line terminators

```
- vemos que se repite lo siguiente e28083 que es un valor unicode que representa el espacio 
- esto da pinta de ser codigo morse o binario
- sustituimos lo valores e28083 por 0 y los 20 por 1
- usamos el siguinete script 
  
  ```python
  from pwn import *
	file = open("whitepages.txt", "rb")
	data = bytearray(file.read())
	data = data.replace(b'\xe2\x80\x83',b'0')
	data = data.replace(b'\x20',b'1')
	
	data = data.decode('ascii')
	data = unbits(data)
	print(data)
  ```
  
  ```
  picoCTF{not_all_spaces_are_created_equal_c54f27cd05c2189f8147cc6f5deb2e56}
  ```
## Notas adicionales
que es unicode?
		es un estandar dentro de las tecnologias de la informacion, para represnetacion y manejo de informacion consiste, pensado en la mayoria de los leguajes del mundo, con todo tipo de caracteres 
UTF-8
		esquema de codificasion de caracteres de longitud variable que ocupa de 1 a 4 bytes para representar un caracter
## Referencias
- https://www.youtube.com/watch?v=427HDV7tzow&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=20

