## Descripción 
Download this disk image and find the flag. Note: if you are using the webshell, download and extract the disk image into /tmp not your home directory.

    Download compressed disk image

## Solución
- se nos da n archivo .mg
- descomprimimos
- usamos mmls para revisar las particiones y vemos que hay 3
```
┌──(kali㉿kali)-[/tmp/...kali]
└─$ fls -o 360448 disk.flag.img
d/d 451:        home
d/d 11: lost+found
d/d 12: boot
d/d 1985:       etc
d/d 1986:       proc
d/d 1987:       dev
d/d 1988:       tmp
d/d 1989:       lib
d/d 1990:       var
d/d 3969:       usr
d/d 3970:       bin
d/d 1991:       sbin
d/d 1992:       media
d/d 1993:       mnt
d/d 1994:       opt
d/d 1995:       root
d/d 1996:       run
d/d 1997:       srv
d/d 1998:       sys
d/d 2358:       swap
V/V 31745:      $OrphanFiles
                             
```

obtenemos '
```
┌──(kali㉿kali)-[/tmp/...kali]
└─$  fls -o 360448 -r disk.flag.img | grep flag
++ r/r * 2082(realloc): flag.txt
++ r/r 2371:    flag.uni.txt
```

solucion
```
┌──(kali㉿kali)-[/tmp/...kali]
└─$     icat -o 360448 disk.flag.img 2371
picoCTF{by73_5urf3r_3497ae6b}

```
## Notas adicionales

## Referencias


