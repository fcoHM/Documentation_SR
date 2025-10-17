

# Linux  Command Line

|  ==Comando==   | Ejemplo                                              | comentarios                                                                                                                                                                                                     |
| :------------: | ---------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|    **grep**    | grep [palabra,frase]  [archivo]                      | esto lo que hace es  buscar una frase o palabra en un dcoumento y regresa todas aquellas lineas que contengan este frase/palabra                                                                                |
|                | -r                                                   | **-r** lo que hace es que la funcion sea recursiva dentro del directorio y sus subdirectorios, si no se especifica la ruta/directorio se asume que es en el actual                                              |
|                | -a                                                   | trata al contenido del archivo como texto                                                                                                                                                                       |
|  **strings**   |                                                      | filtra de los metadatos de un archivo, aquellos que se puedan convertir o son caracteres ascii                                                                                                                  |
|                | -n                                                   | pone una restriccion de tamaño de cadena                                                                                                                                                                        |
| **\|    pipe** | cat [archivo]  \|  grep hola                         | lo que hace es mandar resultados de comandos a alguna direccion o comando especificado                                                                                                                          |
|    **cat**     | cat [archivo]                                        | lo que hace es agarrar todo el contenido del archivo y lo muestra en la terminal                                                                                                                                |
|    **SSH**     | ssh [usuario@host] -p [puerto]                       | SSH es una manera de conectarnos de manera remota a un servidor con solo la terminal especificando el promt con usuario y host, ademas de un  puerto, ademas de que se nos pedira la contraseña de este usuario |
|   **chmod**    | r = 4    <br>w = 2<br>x = 1<br>chmod U/G/O[programa] | en este caso  se tiene que sumar para agregar permisos a ciertos usuarios, ya sea Usuario, Grupo, otros, donde la suma 7 son todos los permiso y se le tiene que asignar                                        |
|     **./**     | sudo ./[programa]                                    | esto es para ejecutar un programa que tenga permisos de ejecusion                                                                                                                                               |
|     **ls**     | ls ~/Downloads/                                      | lista lo que hay en ese directorio                                                                                                                                                                              |
|   **base64**   | base64                                               | para encriptar o descriptar  en base64                                                                                                                                                                          |
|     **wc**     | wc [archivo]                                         | contador                                                                                                                                                                                                        |
|                | git log \| wc -l                                     | en WC sirve pa contar lineas                                                                                                                                                                                    |
|      xxd       | xxe [archivo]                                        | ver los bites de un archivo                                                                                                                                                                                     |
|    hexditor    | hexeditor [archivo]                                  | ver en hexadecimal los valores de un archivo                                                                                                                                                                    |



# NetCat

| Comando | ejemplo                                                                     | comentarios                                                                                        |
| ------- | --------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| nc      | nc jupiter.challenges.picoctf.org 6428<br><br>nc  [direccion.red]  [puerto] | establece una conexion con un servidor por medio de la direccion dada y por un puesto especificado |
|         |                                                                             |                                                                                                    |
# Curl
| **curl** |                                                                                                                                     | hacer requests de headers                           |
| :------: | ----------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- |
|          | -s https://jupiter.challenges.picoctf.org/problem/44573/flag                                                                        | modo silencioso de entrar a una web                 |
|          | -H "Cookie: username-admin; password-hola; admin-True"                                                                              | para mandar un encabezado con una cookie modificada |
|          | -H "User-Agent: picobrowser"                                                                                                        | cambiar el agente o usuario host del cliente        |
|          | -X  GET/POST http://mercury.picoctf.net:28916/index.php?                                                                            | hacer request de metodos GET o POST                 |
|          | -I HEAD http://mercury.picoctf.net:28916/index.php?                                                                                 | hacer requests de metodos HEAD                      |
|          | -d  POST <br>  curl -s https://jupiter.challenges.picoctf.org/problem/39720/login.php -d "username=admin&password=' OR 1 == 1;"<br> | hacer requests con metodos post                     |
|          |                                                                                                                                     |                                                     |



## zsteg

| zsteg |                        | herramienta para aplicar o hacer uso de tecicas de decodificasion de estenografia                                                                                                       |
| ----- | ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|       | zsteg -a buildings.png | -a aplica todas las tecnicas, para obtener un resultado, esto por que no sabemos con que tecnica fue ocultada la informacion, se puede usar en cojunto con grep para filtar informacion |


## PNGCHECK

| pngcheck | pngcheck -v archivo | ver el estado de los archivos png                            |
| -------- | ------------------- | ------------------------------------------------------------ |
|          | -v archivo          | muestra los errores que o defectos que tiene un archvio png  |

## Binwalk

| binwalk | binwalk archivo      | se encarga de nalizar un archivo y  ver si hay algun archivo dentro de este |
| ------- | -------------------- | --------------------------------------------------------------------------- |
|         | binwalk -e [archivo] | extrae cualquier archivo dentro de un archivo                               |
