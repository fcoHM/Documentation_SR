## Descripción 
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29956`.

## Solución
En este caso tube que usar 3 paginas para poder des-ecriptar, una para binario a texto, octal a texto y hexadecimal a texto

teniendo como proceso:

```
Let us see how data is stored
test
Please give the 01110100 01100101 01110011 01110100 as a word.
...
you have 45 seconds.....

Input:
test
Please give me the  164 141 142 154 145 as a word.
Input:
table
Please give me the 70656172 as a word.
Input:
pear
You've beaten the challenge

```

y resultado:

```
Flag: picoCTF{learning_about_converting_values_b375bb16}
```
## Notas adicionales

## Referencias

- https://www.rapidtables.com/convert/number/binary-to-ascii.html
- https://onlinetexttools.com/convert-octal-to-text
- https://www.rapidtables.com/convert/number/hex-to-ascii.html