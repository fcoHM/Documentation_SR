## Descripción 

Can you crack the password to get the flag?Download the password checker here and you'll need the encrypted flag in the same directory too.
## Solución

En este caso se tiene que descargar dos archivos necesarios 

level1.py 
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

flag_enc = open('level1.flag.txt.enc', 'rb').read()


def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "8713"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()

```

level1.flag.txt.enc
```
[gE]__TgS^S

           J                                                                       
```


si nos damos cuenta level1.flag.txt.enc, no nos dice mucho al tratar de analisarlo con cat, pero si ponemos atencion en level1.py podemos darnos cuenta de que este nos va a pedir una contraseña la cual nos debe coincidir con el numero marcado **"8713"**

```python
def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "8713"): #<------aqui
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
```

asi que al ejecutarlo hay que meter ese numero

```
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
```

solucion:
```
picoCTF{545h_r1ng1ng_1b2fd683}
```


