## Descripción 
Help us test the form by submiting the username as test and password as test! The website running here.
## Solución

- iniciamos secion con la cuenta y contraseña
- vemos que si usamos el campo de texto y buscamos no hace nada
- no hay cookies
- pero si regresamos a la pagina de loggin vemos que la primera vez aparece una ventana en blanco, pero se vemos la url sale un id con algo que parece base64
 ```
 bF90aGVfd2F5X2JlNzE2ZDhlfQ== -----> l_the_way_be716d8e}
 ```
y si regresamos una vez mas sale lo mismo pero diferente id
```
cGljb0NURntwcm94aWVzX2Fs -------> picoCTF{proxies_al
```

las ordenamos y queda de la siguiente manera
```
picoCTF{proxies_all_the_way_be716d8e}
```
