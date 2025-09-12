## Descripción 
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...
## Solución
misma solucion que 17-Tab, Tab, Attack solo que aqui al no ser directorio no se usa la funcion recursiva -r

```bash
grep -a "pico" warm
```

aplicando eso nos da lo siguinete
```
]��f.�]�@f.�H�=� H��t    H�5�    UH)�H��H��H��H��?H�H��t▒H��     H��t
                                                                     ]��f�]�@f.��=y      u/H�=W  UH��t
����H����Q       ]����fDUH��]�f���UH��H���}�H�u��}�uH�=�������KH�E�H�H�H�5�H���������uH�=��i����H�E�H�H�H��H�=:��X������DAWAVI��AUATL�%F UH�-F SA��I��L)�H�H�������H��t 1��L��L��D��A��H��H9�u�H�[]A\A]A^A_Ðf.���H�H��Hello user! Pass me a -h to learn what I can do!-hOh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}I don't know what '%s' means! I do know what -h means though!
                                                           
```

donde la solucion es 
```
picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
```
## Notas adicionales

## Referencias

- problemas anteriores 
- https://es.stackoverflow.com/questions/855/c%C3%B3mo-convertir-un-archivo-binario-a-ascii-en-unix

## comentarios
sinceramente creo que no se resulve asi, o eso asumo por las 5 pistas que da que quiren que descarge un archivo, le de permisos y con eso lo ejecute 

pero aqui esta la forma  que pide 
```
┌──(kali㉿kali)-[~/Downloads]
└─$ chmod 5 warm 

┌──(kali㉿kali)-[~/Downloads]
└─$ ls -al

-------r-x  1 kali kali   10936 Sep  4 22:41 warm

┌──(kali㉿kali)-[~/Downloads]
└─$ sudo ./warm 
Hello user! Pass me a -h to learn what I can do!

┌──(kali㉿kali)-[~/Downloads]
└─$ sudo ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}


```