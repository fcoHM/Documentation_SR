## Descripción 
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)Access checker program: `nc saturn.picoctf.net 61707`
## Solución
- descomprimirmos con gunzip
```
gunzip disk.img.gz 
```

- usamos mmls y le mandamos la particion de linux
```
┌──(kali㉿kali)-[~/Downloads]
└─$ nc saturn.picoctf.net 61707
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}

```
## Notas adicionales

## Referencias


