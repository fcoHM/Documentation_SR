## Descripción 
Decode this message from the moon.
## Solución
se nos da un archivo de audio 
- revisamos el audio y no hay nada que nos interese
- lo abrimos y efectivamente es audio con ciertas freacuencias raras
- usamos SSTV decoder  la cual tiene 3 opciones de decodificasion (Martin 1.2, Scotie 1.2 DX, Robot 36 .72) pero usaremos la de scotie ya que la pista pregunta por la mascota y este es el nombre de la mascota
ejecutamos el  siguinete codigo

```bash
sstv -d message.wav -o flag.png
```

![[moowalk.png]]
solucion:
```
picoCTF{beep_boop_im_in_space}
```
## Notas adicionales
como llegaron las primeras fotos de la luna a la tierra?
		el apolo 11 tenia camaras de television monocromaticas que usava un formato llamado SSTV a 10 frames por segundo  com 320 lineas de resolucion y viajaba en forma de audio
## Referencias


