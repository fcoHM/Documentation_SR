## Descripción 
This is a really weird text file TXT? Can you find the flag?
## Solución

Como se identifica que tipo de archivo es???
- en la cabecera de los archivos existen unos bites(magic bites) estos son indicativos de que tipo de archivo se trata, una especie de archivo
- en este caso si revisamos la cabecera en hexadecimal del archivo flag.txt en realidad es un png
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ xxd flag.txt|head
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG........IHDR
00000010: 0000 06a1 0000 0260 0802 0000 0085 ad5e  .......`.......^
00000020: 9a00 0000 0173 5247 4200 aece 1ce9 0000  .....sRGB.......
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...
00000040: 0009 7048 5973 0000 1625 0000 1625 0149  ..pHYs...%...%.I
00000050: 5224 f000 0026 9549 4441 5478 5eed dd6b  R$...&.IDATx^..k
00000060: 421b 39b7 05d0 3b2e 0694 f130 9a4c 2683  B.9...;....0.L&.
00000070: f9ae 5f80 4e3d 25bb 4cb3 f15a bfba a14a  .._.N=%.L..Z...J
00000080: 7574 2413 7927 c0ff fd0f 0000 0000 4826  ut$.y'........H&
00000090: e303 0000 0080 6c32 3e00 0000 00c8 26e3  ......l2>.....&.

```

le colocaremos correctamente la extencion 
```bash
mv flag.txt flag.png
```

lo que da como resultado 
```
picoCTF{now_you_know_about_extensions}
```
## Notas adicionales
- Firmas de Archivos (Magic Numbers)

| Formato | Extensión    | Firma (Hexadecimal)                 | Descripción                        |
| ------- | ------------ | ----------------------------------- | ---------------------------------- |
| JPEG    | .jpg / .jpeg | FF D8 FF                            | Imagen JPEG                        |
| PNG     | .png         | 89 50 4E 47 0D 0A 1A 0A             | Imagen PNG                         |
| GIF     | .gif         | 47 49 46 38                         | Imagen GIF (GIF87a o GIF89a)       |
| BMP     | .bmp         | 42 4D                               | Imagen Bitmap                      |
| TIFF    | .tif / .tiff | 49 49 2A 00 ó 4D 4D 00 2A           | Imagen TIFF (little/big endian)    |
| PDF     | .pdf         | 25 50 44 46                         | Documento PDF                      |
| ZIP     | .zip         | 50 4B 03 04                         | Archivo comprimido ZIP             |
| RAR     | .rar         | 52 61 72 21 1A 07 00                | Archivo RAR v1.5-4.x               |
| RAR     | .rar         | 52 61 72 21 1A 07 01 00             | Archivo RAR v5.0+                  |
| 7-Zip   | .7z          | 37 7A BC AF 27 1C                   | Archivo 7-Zip                      |
| GZIP    | .gz          | 1F 8B                               | Archivo GZIP                       |
| TAR     | .tar         | 75 73 74 61 72                      | "ustar" en cabecera (posición 257) |
| MP3     | .mp3         | FF FB                               | Audio MPEG Layer III               |
| WAV     | .wav         | 52 49 46 46 xx xx xx xx 57 41 56 45 | Audio WAV                          |
| AVI     | .avi         | 52 49 46 46 xx xx xx xx 41 56 49 20 | Video AVI                          |
| MP4     | .mp4 / .m4v  | 00 00 00 18 66 74 79 70             | Video MP4                          |
| MOV     | .mov         | 00 00 00 14 66 74 79 70 71 74 20 20 | Video MOV (QuickTime)              |
| EXE     | .exe         | 4D 5A                               | Ejecutable PE/DOS ("MZ")           |
| DLL     | .dll         | 4D 5A                               | Biblioteca de Windows              |
| ELF     | (Linux)      | 7F 45 4C 46                         | Ejecutable ELF (Linux/Unix)        |
| ISO     | .iso         | 43 44 30 30 31                      | Imagen ISO9660 (CD-ROM)            |
| DOC     | .doc         | D0 CF 11 E0 A1 B1 1A E1             | Documento MS Office antiguo (OLE2) |
| DOCX    | .docx        | 50 4B 03 04                         | Documento Office Open XML (ZIP)    |
| XLSX    | .xlsx        | 50 4B 03 04                         | Hoja de cálculo Office Open XML    |
| PPTX    | .pptx        | 50 4B 03 04                         | Presentación Office Open XML       |

## Referencias
- https://www.youtube.com/watch?v=FbFpIS60M_s&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=17
- 