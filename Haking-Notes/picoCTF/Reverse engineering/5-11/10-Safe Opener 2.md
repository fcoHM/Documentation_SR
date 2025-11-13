## Descripción 
What can you do with this file? I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/287/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
## Solución
- se nos da un archivo .class
- lo que hacemos aqui es decompular con javap -v para una version detallada y encontramos lo siguiente 
  ```
  #93 = Utf8               picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_b427942b}
  ```

```bash
# Desde la terminal/CMD
javap -c NombreArchivo.class    # Muestra bytecode
javap -p NombreArchivo.class    # Muestra miembros privados
javap -v NombreArchivo.class    # Información detallada
```
## Notas adicionales

# Referencias
