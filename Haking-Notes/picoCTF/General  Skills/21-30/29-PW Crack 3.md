## Descripción 

Can you crack the password to get the flag?Download the password checker here and you'll need the encrypted flag and the hash in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
Para este caso toco rtevisar el codigo que proporciona 

level3.py
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

flag_enc = open('level3.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level3.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_3_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_3_pw_check()


# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]

```


sis nos fijamos hay una lista de posibles contraseñas 
```python
# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]
```

teniendo en cuenta esto nos podemos solo enfocarnos en eso, y volvemos a los casos 25-PW Crack 1 y 26-PW Crack 2, que como sabemos se obtiene la llave comparando una clabe existente con una externa

por lo caul le vamos a hacer adaptaciones al codigo para hacer fuerza bruta y probar todas las llaves y nos diga cual fue la llave que funciono 

```python
# ahora esta va antes de la llamada de la funcion  para que sea un recurso global
pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]

# hacemos que funcion reciba un parametro y en ves de in input ponemos ese parametro

def level_3_pw_check(llave): 
    user_pw = llave #<----- tal que asi
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print(llave) #<------ nos dice la llave que funciono
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
    
    
#ponemos en ciclo totas las posibles lleves
for pw in pos_pw_list:
    level_3_pw_check(pw)
```

solucion:
```
That password is incorrect
That password is incorrect
That password is incorrect
That password is incorrect
That password is incorrect
That password is incorrect
865e  <-------llave que si accedio
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
```


