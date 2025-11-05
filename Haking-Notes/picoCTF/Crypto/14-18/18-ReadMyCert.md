## Descripción 
How about we take you on an adventure on exploring certificate signing requests Take a look at this CSR file [here](https://artifacts.picoctf.net/c/423/readmycert.csr).
## Solución
- se nos da un .csr
- usamo el siguiente comando para investigarlo 
```
openssl req -in readmycert.csr -noout -text
```

- en el encabezado podemos ver lo siguiente
```
Subject: CN = picoCTF{read_mycert_57f58832}
```
## Notas adicionales
que es un csr?
Un archivo .csr, o solicitud de firma de certificado (Certificate Signing Request), es un bloque de texto cifrado que se genera normalmente en el servidor donde se instalará un certificado SSL/TLS, aunque también puede crearse externamente utilizando herramientas específicas
# Referencias
