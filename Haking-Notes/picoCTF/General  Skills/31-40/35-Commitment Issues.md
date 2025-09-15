## Descripción 
I accidentally wrote the flag down. Good thing I deleted it! You download the challenge files here:
## Solución
En este caso fue muy sencillo ya que no habia mas ramas y solo habia dos commits por locual se investigo en el primero, pero no habia nada, por lo cual se hizon un cambio de commit para revisar cambios 

```bash
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git checkout 3d5ec8a26ee7b092a1760fea18f384c35e435139

Note: switching to '3d5ec8a26ee7b092a1760fea18f384c35e435139'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 3d5ec8a create flag

┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git log                                              
commit 3d5ec8a26ee7b092a1760fea18f384c35e435139 (HEAD)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:14 2024 +0000

    create flag

┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ ls
message.txt

┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ cat message.txt 
picoCTF{s@n1t1z3_30e86d36}
```

dando como respuesta 
```
picoCTF{s@n1t1z3_30e86d36}
```
## Notas adicionales

## Referencias

- documentacion de git