## Descripción 

Can you crack the password to get the flag?Download the password checker here and you'll need the encrypted flag in the same directory too.
## Solución

Este caso fue muy similar a 25-PW Crack 1 ya que la solucion es la misma, pide una contraseña la cual se va a comparar con un algo que este caso es un valor cifrado en hexadecimal 

level2.py
```python
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level2.flag.txt.enc', 'rb').read()

def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_2_pw_check()

```

y practicamente el otro archivo es pura distraccion, por lo cual nos vamos directo sobre la comparacion  donde si cortamos la parte de la comparacion y la pasmo a python nos dara la contraseña con la cual se espera comparar

```python
if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ): #<--- esto
```

donde:
```python
chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) # es igual a "de76"
```

solucion:
```
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}

```
## Referencias

- 25-PW Crack 1
