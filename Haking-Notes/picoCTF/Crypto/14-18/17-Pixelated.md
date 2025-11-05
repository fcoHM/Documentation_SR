## Descripción 
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/6e4afb967ef8c865f79f3a8cd7767cca/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/6e4afb967ef8c865f79f3a8cd7767cca/scrambled2.png)
## Solución
- se no da la siguientes imagenes 
![[Pasted image 20251104195354.png]]

- se convino las imagenes con el siguiente script 
  ```python
from PIL import Image # pip install Pillow
img1 = Image.open("scrambled1.png")
pixels1 = img1.load()
img2 = Image.open("scrambled2.png")
pixels2 = img2.load()
flag = Image.new("RGB", img1.size)
flagpix = flag.load()

for row in range(img1.size[1]):

	for col in range(img1.size[0]):
		flagpix[col, row] = (	
		(pixels1[col, row][0] + pixels2[col, row][0]) % 256,
		(pixels1[col, row][1] + pixels2[col, row][1]) % 256,
		(pixels1[col, row][2] + pixels2[col, row][2]) % 256
		)

flag.save("flag.png")
  ```

- dando como resultado 
![[Pasted image 20251104200012.png]]

solucion:
```
picoCTF{0542dc1d}
```
## Notas adicionales

# Referencias
- nada que ver pero este rolon se llama casi igual jajajajajaja
  https://www.youtube.com/watch?v=AeO81mfRook&list=RDAeO81mfRook&start_radio=1