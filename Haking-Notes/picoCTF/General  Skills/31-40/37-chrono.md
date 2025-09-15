## Descripción 
How to automate tasks to run at intervals on linux servers?
Additional details will be available after launching your challenge instance.

How to automate tasks to run at intervals on linux servers? Use ssh to connect to this server:
Server: saturn.picoctf.net
Port: 51453
Username: picoplayer 
Password: kZx-HVJKu8

## Solución
Bueno en este caso al estar hablando de cron se intuye que debe de haber archivos que los configuran, por lo cual en etc nos dsiponemos a buscar eso archivos

```bash
picoplayer@challenge:~$ ls -l /etc/ | grep cron
drwxr-xr-x 1 root   root       26 Aug  4  2023 cron.d
drwxr-xr-x 1 root   root       26 Aug  4  2023 cron.daily
drwxr-xr-x 2 root   root       26 Aug  4  2023 cron.hourly
drwxr-xr-x 2 root   root       26 Aug  4  2023 cron.monthly
drwxr-xr-x 2 root   root       26 Aug  4  2023 cron.weekly
-rw-r--r-- 1 root   root       43 Aug  4  2023 crontab
```

una vez indetificados procedemos nos damos cuenta de que unicamente hay uno que es un archivo, asi que los revisamos

```bash
picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
```

y he ahi, donde solo una de las coaas que referencia y es un arcgico es crontab
lo cual nos da la solucion 

solucion:
```
picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
```
## Notas adicionales

## Referencias

- https://es.wikipedia.org/wiki/Cron_(Unix)