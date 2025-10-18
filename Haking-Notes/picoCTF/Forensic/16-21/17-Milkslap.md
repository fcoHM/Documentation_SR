## Descripción 
🥛
## Solución
- se nos porporciona una pagina
- revisamos el html y vemos que hay un archivo .js
- vemos que el .js controla el gif de la pagina cada vez que le pasamos el mouse por encima
- usamos ctr+i para ver el panel de ayuda que nos muestra la imagen, ya que no se puede descargar de manera normal y una vez ahi se descarga la imagen
- usamos zsteg para ver que hay, pero antes hay que modificar el buffer ya que la imagen es muy pesada 
```bash
export RUBY_THREAD_VM_STACK_SIZE=500000000 
zsteg concat_v.png
```

solucion:
```
picoCTF{imag3_mén1pul4t10n_s14p5}
```
## Notas adicionales
- este me dio error por iteracion infinita pero se resuelve con zsteg


