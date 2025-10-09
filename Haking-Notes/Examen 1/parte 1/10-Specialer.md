## Descripción 
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer. ssh -p 64191 ctf-player@saturn.picoctf.net. The password is d8819d45
## Solución
En este caso vemos que no pododemo usar bash 
- lo que hacemo es usar doble tam al inicar la terminal ya que esto nos dara los comando que podemos usar
  
  ```bash
  Specialer$ 
!          break      coproc     esac       function   local      return     times      wait
./         builtin    declare    eval       getopts    logout     select     trap       while
:          caller     dirs       exec       hash       mapfile    set        true       {
[          case       disown     exit       help       popd       shift      type       }
[[         cd         do         export     history    printf     shopt      typeset    
]]         command    done       false      if         pushd      source     ulimit     
alias      compgen    echo       fc         in         pwd        suspend    umask      
bash       complete   elif       fg         jobs       read       test       unalias    
bg         compopt    else       fi         kill       readarray  then       unset      
bind       continue   enable     for        let        readonly   time       until 
  ```

en este caso usamos echo para ver archivos y ver que es lo que hay en carpetas y para movernos entre carpeta usaremos cd 
```bash

Specialer$ echo *
abra ala sim
Specialer$ cd abra
Specialer$ echo *   
cadabra.txt cadaniel.txt
Specialer$ cd
Specialer$ cd home
-bash: cd: home: No such file or directory
Specialer$ cd /home
Specialer$ echo *
ctf-player
Specialer$ cd ctf-player/
Specialer$ echo *
abra ala sim
Specialer$ cd ala
Specialer$ echo *
kazam.txt mode.txt
Specialer$ echo kazam.txt 
kazam.txt
Specialer$ echo read kazam.txt 
read kazam.txt
Specialer$ read kazam.txt 
-bash: read: `kazam.txt': not a valid identifier
Specialer$ echo $(<kazam.txt)
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_c42168d9}
```


la experesion echo $(< archivo.txt) es para que el contenido lo mande en pantalla
