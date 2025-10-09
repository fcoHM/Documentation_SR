## Descripción 
Can you abuse the banner? The server has been leaking some crucial information on tethys.picoctf.net 56955. Use the leaked information to get to the server. To connect to the running application use nc tethys.picoctf.net 49797. From the above information abuse the machine and find the flag in the /root directory.
## Solución
- nos conectamos a la primera dirreccion y nos dan una contraseña
```
SSH-2.0-OpenSSH_7.6p1 My_Passw@rd_@1234
```

- nos ocnectamos a la siguinete dirreccion y nos pide una preguntas que si respondemos bien nos abre la termina
- buscamos la bandera pero no hay nada 
- revisamos que la carpeta de root y vemos que ahi esta la flag pero no podemos abrirla ni revisarla
- hay un archivo python que es el programa que se ejecuta apenas te conectas, si lo revisamos nos suguiere que remplacemos el archivo banner de usuario por la flag
```python
if __name__ == "__main__":
    try:
      with open("/home/player/banner", "r") as f:
        print(f.read())
    except:
      print("*********************************************")
      print("***************DEFAULT BANNER****************")
      print("*Please supply banner in /home/player/banner*")
      print("*********************************************")

try:
    request = input("what is the password? \n").upper()
    while request:
        if request == 'MY_PASSW@RD_@1234':
            text = input("What is the top cyber security conference in the world?\n").upper()
            if text == 'DEFCON' or text == 'DEF CON':
                output = input(
                    "the first hacker ever was known for phreaking(making free phone calls), who was it?\n").upper()
                if output == 'JOHN DRAPER' or output == 'JOHN THOMAS DRAPER' or output == 'JOHN' or output== 'DRAPER':
                    scmd = 'su - player'
                    pty.spawn(scmd.split(' '))

                else:
                    print(incorrect_ans_reply)
            else:
                print(incorrect_ans_reply)
        else:
            print(incorrect_ans_reply)
            break

except:
    KeyboardInterrupt


```

- lo hacemos y obtenemos
```
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_f7608541}
```

