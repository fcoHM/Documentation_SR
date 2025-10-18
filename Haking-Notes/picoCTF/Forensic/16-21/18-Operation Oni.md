## Descripción 
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download disk image](https://artifacts.picoctf.net/c/71/disk.img.gz)
- Remote machine: `ssh -i key_file -p 59486 ctf-player@saturn.picoctf.net`
## Solución
- optenemos un archivo .img
- usamos herramienta autopsy
- usamos mmls para analizar la informacion de la imagen
```
┌──(kali㉿kali)-[~/Downloads]
└─$ mmls disk.img      
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)

```
- usando fls que nos permite dicatar los directorios dentro de la imagen
```
┌──(kali㉿kali)-[~/Downloads]
└─$ fls -o 206848 disk.img 
d/d 458:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib
d/d 85: var
d/d 94: usr
d/d 104:        bin
d/d 118:        sbin
d/d 464:        media
d/d 468:        mnt
d/d 469:        opt
d/d 470:        root
d/d 471:        run
d/d 473:        srv
d/d 474:        sys
V/V 33049:      $OrphanFiles
                              
```

- para acceder a carepetas entramos poneiendo el numero de la carepeta al final 
```
┌──(kali㉿kali)-[~/Downloads]
└─$ fls -o 206848 disk.img 470
r/r 2344:       .ash_history
d/d 3916:       .ssh
                        
```

- para ver el contenido de los archivos usamos icat que es lo mismo que un cat pero para archivos con particion
- obtenemos la llave privada
```
┌──(kali㉿kali)-[~/Downloads]
└─$ icat -o 206848 disk.img 2345 >key_file
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----
```

- de damos permisos de solo escritura al nuevo archivo
```bash
chmod 400 key_file
```

- no logeamos

solucion:
```
picoCTF{k3y_5l3u7h_af277f77}
```
## Notas adicionales

## Referencias

- https://www.youtube.com/watch?v=PVeV-S3Zbqk&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=32&t=308s
