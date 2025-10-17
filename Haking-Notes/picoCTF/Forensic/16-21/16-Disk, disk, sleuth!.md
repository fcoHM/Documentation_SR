## Descripción 
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: dds1-alpine.flag.img.gz
## Solución
- se nos porporciono un archivo con multiples extenciones
- descomprimimos el archivo ya que la ultima extencion es en un .gz
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ gzip -d dds1-alpine.flag.img.gz 
```

- se nos hace incistenacia de usar `srch_strings`
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ srch_strings dds1-alpine.flag.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_a011c142}
```

solucion:
```
picoCTF{f0r3ns1c4t0r_n30phyt3_a011c142}
```
## Notas adicionales
srch_strings - Display printable strings in files 
## Referencias

- https://manpages.debian.org/jessie/sleuthkit/srch_strings.1.en.html
