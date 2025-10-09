## Descripción 
Why search for the flag when I can make a bookmarklet to print it for me? Browse here, and find the flag!
## Solución
cuando abrimos la web vemos que se dejo expuertos codigo de java script en un campo de texto
- lo copiamos y lo intentamos ejecutar en la consola del navegador
  
  ```javascript
    javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÒËÉ§©í";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
    
  ```
  
  - dio como resultado:
    ```
    picoCTF{p@g3_turn3r_6bbf8953}
    ```

