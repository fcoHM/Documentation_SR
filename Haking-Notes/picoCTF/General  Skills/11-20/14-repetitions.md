## Descripción 
Can you make sense of this file?
	download the file
## Solución
Este  caso lo que tiene es que esta en base 64, aun que tiene algo peculiar  y ese algo peculiar es que es muy largo, lo que suguire que esta mas de una sola vez encriptado en base 64 por lo cual usamos un cat para optener el contenido del archivo y con un grep se lo pasamos a base64  y con la opcion -d de que es para decodificar

```bash
cat end_flag | base64 -d
```

y cada vez la cadena se va haciendo mas pequeña lo cual no indica que un falta por decodificar 
por lo cual le psamos el resultado de la deodificasion a base64 -d otra vez 

quedando de la siguinete manera:
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ cat enc_flag      
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbHBWV0VKVVZGWmFWMDVHV2tkYVNHUlZDazFyY0ZkVWJGWlhZVlpLU0dWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==

┌──(kali㉿kali)-[~/Downloads]
└─$ cat enc_flag | base64 -d
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlpVWEJUVFZaV05GWkdaSGRVCk1rcFdUbFZXYVZKSGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg==


┌──(kali㉿kali)-[~/Downloads]
└─$ cat enc_flag | base64 -d | base64 -d
V1RCa2MyRnRTWGRVYkZaVFltNVNjRmRXYUU5aVJUVnhWVzFhYVdGck5UWmFSVkpQWVRGbmVWVnVR
bHBsYTBweVUxWmpNRTVHWjNsVgpXR1JyVFdwV2VsUlZVbE5oTURCNVZXMWFZUXBTTVZWNFZGZHdU
MkpWTlVWaVJHeEVXbm93T1VOblBUMEsK

┌──(kali㉿kali)-[~/Downloads]
└─$ cat enc_flag | base64 -d | base64 -d|base64 -d
WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aYQpSMVV4VFdwT2JVNUViRGxEWnowOUNnPT0K

┌──(kali㉿kali)-[~/Downloads]
└─$ cat enc_flag | base64 -d | base64 -d|base64 -d|base64 -d
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZa
R1UxTWpObU5EbDlDZz09Cg==

┌──(kali㉿kali)-[~/Downloads]
└─$ cat enc_flag | base64 -d | base64 -d|base64 -d|base64 -d|base64 -d
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfZGU1MjNmNDl9Cg==

┌──(kali㉿kali)-[~/Downloads]
└─$ cat enc_flag | base64 -d | base64 -d|base64 -d|base64 -d|base64 -d|base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_de523f49}

```

teniendo que decodificar hasta 6 veces para llegar a la flag

```
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_de523f49}
```
## Notas adicionales

## Referencias

- comandos previos usados y de los enciados en classrrom
- https://base64.guru/
