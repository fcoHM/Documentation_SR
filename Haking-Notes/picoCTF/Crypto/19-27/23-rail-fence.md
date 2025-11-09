## Descripción 
A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it? Download the message [here](https://artifacts.picoctf.net/c/190/message.txt). Put the decoded message in the picoCTF flag format, `picoCTF{decoded_message}`.
## Solución
- se nos duio un archivo con el siguiente contenido 
```
Ta _7N6DDDhlg:W3D_H3C31N__0D3ef sHR053F38N43D0F i33___NA
```

- usamos una pagina para en contrar la flag y encontramos esto
```
The flag is: WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_D00AFDD3
```

solucion:
```
picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_D00AFDD3}
```
## Notas adicionales
- Rail fence cipher:is a [classical](https://en.wikipedia.org/wiki/Classical_cipher "Classical cipher") type of [transposition cipher](https://en.wikipedia.org/wiki/Transposition_cipher "Transposition cipher"). It derives its name from the manner in which encryption is performed, in analogy to a fence built with horizontal rails.
# Referencias
- https://www.boxentriq.com/code-breaking/rail-fence-cipher