## Descripción 
A second message has come in the mail, and it seems almost identical to the first one. Maybe the same thing will work again. Download the message [here](https://artifacts.picoctf.net/c/183/message.txt).
## Solución
- se nos dat un .txt copn la siguinete informacion
  ```
  LKOb (bwvek ove lgqkhej kwj osgx) gej g kyqj vo lvrqhkje bjlhetky lvrqjktktvu. Lvukjbkgukb gej qejbjukjz dtkw g bjk vo lwgssjuxjb dwtlw kjbk kwjte lejgktftky, kjlwutlgs (guz xvvxstux) bitssb, guz qevmsjr-bvsftux gmtstky. Lwgssjuxjb hbhgssy lvfje g uhrmje vo lgkjxvetjb, guz dwju bvsfjz, jglw ytjszb g bketux (lgssjz g osgx) dwtlw tb bhmrtkkjz kv gu vustuj blvetux bjeftlj. LKOb gej g xejgk dgy kv sjgeu g dtzj geegy vo lvrqhkje bjlhetky bitssb tu g bgoj, sjxgs juftevurjuk, guz gej wvbkjz guz qsgyjz my rguy bjlhetky xevhqb gevhuz kwj dvesz ove ohu guz qeglktlj. Ove kwtb qevmsjr, kwj osgx tb: qtlvLKO{OE3AH3ULY_4774LI5_4E3_L001_6J0659OM}
  ```

por lo visto es muy similar al anterior
- se lo damos a la pagina y nos da lo siguiente 
```
PICOCTF{FR3JU3NCY_4774CK5_4R3_C001_6E0659FB}
```

pero este es incorrecto ya que en desencriptador tuvo errores con la j en esta parte FR3JU3NCY, tenia que se una Q

solucion:
```
picoCTF{FR3QU3NCY_4774CK5_4R3_C001_6E0659FB}
```
## Notas adicionales

# Referencias
- https://www.dcode.fr/monoalphabetic-substitution