## Descripción 
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: Addadshashanammu.zip
## Solución
bueno en este caso se uso unzip para poder acceder al directorio

```bash
unzip 
```

una vez teniendo el diccionario utilizamos la misma tecnica que anteriormente hemos usado 

```bash
grep -ar Addadshashanammu/
```

donde -a previamente mencionamos que era para hacer que lea el binario como texto y -r para que fuera recursivo en los subdirectorios, doando como resultado 

```
Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet: u/H�=�      UH��t
����H�����       ]����fDUH��]�f���UH��H�=�������]�f.�DAWAVI��AUATL�%F UH�-F SA��I��L)�H�H���W���H��t 1��L��L��D��A��H��H9�u�H�[]A\A]A^A_Ðf.���H�H��*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}<��������▒���X"����H��������0zRx
                                                                                                                                                                                                                                 ����+zRx
                                                                                                                                                                                                                                        $X��� F▒J
R    �?▒;*3$"DP��\R���A�C
D|X���eB�B▒�E �B(�H0�H8�M@r8A0A(B B▒B�����0�
���o�`�   
```

donde lo importante es lo siguiente:

```
picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}
```
## Notas adicionales

## Referencias

- comando previos ya usados en problemas pasados
