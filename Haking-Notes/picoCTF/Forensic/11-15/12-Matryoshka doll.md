## Descripción 
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: this
## Solución
- se nos dio una imagen "dolls.jpg" 
- si hacemos cat no hay nada 
- si revisamos la foto esta intacta
- si hacemos una exiftool  para ver lo metadatos no vemos nada interesante
- si hacemos un strings a los primeros 10 renglones vemos algo curioso, pareciera haber un archivo dentro de la imagen
```
iTXtXML:com.adobe.xmp
<x:xmpmeta xmlns:x="adobe:ns:meta/" x:xmptk="XMP Core 5.4.0">
   <rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#">
      <rdf:Description rdf:about=""
            xmlns:exif="http://ns.adobe.com/exif/1.0/">
         <exif:PixelXDimension>594</exif:PixelXDimension>
         <exif:UserComment>Screenshot</exif:UserComment>
         <exif:PixelYDimension>1104</exif:PixelYDimension>
      </rdf:Description>
   </rdf:RDF>
</x:xmpmeta>
IDEEb^*Qcb4
Z9vT?vA/_$
a#;s;[gyjD
n3zY[>GAD
=,e< =*?Yp
3Sn'&bbGf'
\sMKn$R`eG
~wkwwG;~A
base_images/2_c.jpgUT    <-------------- aqui 
C}-Zjvj"""Z
/\6c7l*18Mj
Hr~& 8Ja7i,
t+Vp`B2AYq
se\45~|_4Z
%(oQ1y~?e?
Db^!u"tE=O
9)IZ9Rj|Fn
|YrAkJI_S,
cG3CKkcs3G
=T*N+b_Io8
-8(Ly<7-"`
kT_S0/,0L3
mlKszlh<f$
>,\vxk~[        .R
l_(ZU2&?IX
>KO<K-j3|sD
C#CgS}K[CsSgF6}c
base_images/2_c.jpgUT   <-------------- y aqui
```

- com binwalk podemos confirmar esto
```bash
binwalk dolls.jpg
```

- obtenemos lo siguiente
```
DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378952, uncompressed size: 383937, name: base_images/2_c.jpg
651610        0x9F15A         End of Zip archive, footer length: 22

```


- nos da una imagen que esta dentro de un zip, y si la abrimos vemos que es otra muñeca, por lo cual si repetimos el procedimiento vemos que hay otro archivo dentro de esta imagen 
```bash
┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted]
└─$ ls
4286C.zip  base_images  ime2

┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted]
└─$ open ime2     

┌──(kali㉿kali)-[~/Downloads/_dolls.jpg.extracted]
└─$ binwalk ime2        

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196042, uncompressed size: 201444, name: base_images/3_c.jpg
383804        0x5DB3C         End of Zip archive, footer length: 22
383915        0x5DBAB         End of Zip archive, footer length: 22
```

- repetimos el problema hasta encontrar  la flag, que en este caso es un .txt 
```
picoCTF{96fac089316e094d41ea046900197662}
```
## Notas adicionales

## Referencias

- https://www.youtube.com/watch?v=NkbtA7x5aVI&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=26
