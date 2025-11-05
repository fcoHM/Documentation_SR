## Descripción 
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/238/atbash.jpg).
## Solución
- se nos da la siguiente imagen 
  ![[Pasted image 20251104193328.png]]
-  revisamos la foto y vemos que no no hay nada legible con cat
- revisamos con binwalk y no hay nada 
- usando steghide, no da lo siguiente
  ```bash
  steghide extract -sf atbash.jpg
 krxlXGU{zgyzhs_xizxp_8z0uvwwx}
  ```

- usanod cyberchef des encriptamos con  atbash
- y obtenemos la siguinete solucion
```
 picoCTF{atbash_crack_8a0feddc}
```
## Notas adicionales
steghide:
como se instala 
```bash
sudo apt install steghide   
```
# Referencias
- https://www.youtube.com/watch?v=yNFrsb5T5_s