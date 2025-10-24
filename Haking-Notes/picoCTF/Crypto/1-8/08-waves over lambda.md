## Descripción 
We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with `nc jupiter.challenges.picoctf.org 43522`.
## Solución
- nos conectamos y nos da el siguinete texto que parece viginier
```
-------------------------------------------------------------------------------
pmvzxgbn cuxu yn dmsx rlgz - rxuasuvpd_yn_p_moux_lgfiwg_mzrfgsvxgr
-------------------------------------------------------------------------------
gluqud rdmwmxmoybpc tgxgfgemo kgn bcu bcyxw nmv mr rdmwmx jgolmoybpc tgxgfgemo, g lgvw mkvux kull tvmkv yv msx wynbxypb yv cyn mkv wgd, gvw nbyll xufufiuxuw gfmvz sn mkyvz bm cyn zlmmfd gvw bxgzyp wugbc, kcypc cgjjuvuw bcyxbuuv dugxn gzm, gvw kcypc y ncgll wunpxyiu yv ybn jxmjux jlgpu. rmx bcu jxunuvb y kyll mvld ngd bcgb bcyn lgvwmkvuxrmx nm ku snuw bm pgll cyf, glbcmszc cu cgxwld njuvb g wgd mr cyn lyru mv cyn mkv unbgbukgn g nbxgvzu bdju, dub mvu jxubbd rxuasuvbld bm iu fub kybc, g bdju gihupb gvw oypymsn gvw gb bcu ngfu byfu nuvnulunn. isb cu kgn mvu mr bcmnu nuvnulunn juxnmvn kcm gxu ouxd kull pgjgilu mr lmmtyvz grbux bcuyx kmxlwld grrgyxn, gvw, gjjgxuvbld, grbux vmbcyvz ulnu. rdmwmx jgolmoybpc, rmx yvnbgvpu, iuzgv kybc vuqb bm vmbcyvz; cyn unbgbu kgn mr bcu nfgllunb; cu xgv bm wyvu gb mbcux fuv'n bgilun, gvw rgnbuvuw mv bcuf gn g bmgwd, dub gb cyn wugbc yb gjjugxuw bcgb cu cgw g csvwxuw bcmsngvw xmsilun yv cgxw pgnc. gb bcu ngfu byfu, cu kgn gll cyn lyru mvu mr bcu fmnb nuvnulunn, rgvbgnbypgl rullmkn yv bcu kcmlu wynbxypb. y xujugb, yb kgn vmb nbsjywybdbcu fghmxybd mr bcunu rgvbgnbypgl rullmkn gxu ncxukw gvw yvbullyzuvb uvmszcisb hsnb nuvnulunnvunn, gvw g jupslygx vgbymvgl rmxf mr yb.
```
- este es un cifrado de sustitucion
- no tenemos llave por lo que tenemos que hacer fuerza bruta 
- obtenemos lo siguinente
```
congrats here is your flag - frequency_is_c_over_lambda_ogfmaunraf
-------------------------------------------------------------------------------
alexey fyodorovitch karamazov was the third son of fyodor pavlovitch karamazov, a land owner well known in our district in his own day, and still remembered among us owing to his gloomy and tragic death, which happened thirteen years ago, and which i shall describe in its proper place. for the present i will only say that this landownerfor so we used to call him, although he hardly spent a day of his life on his own estatewas a strange type, yet one pretty frequently to be met with, a type abject and vicious and at the same time senseless. but he was one of those senseless persons who are very well capable of looking after their worldly affairs, and, apparently, after nothing else. fyodor pavlovitch, for instance, began with next to nothing; his estate was of the smallest; he ran to dine at other men's tables, and fastened on them as a toady, yet at his death it appeared that he had a hundred thousand roubles in hard cash. at the same time, he was all his life one of the most senseless, fantastical fellows in the whole district. i repeat, it was not stupiditythe majority of these fantastical fellows are shrewd and intelligent enoughbut just senselessness, and a peculiar national form of it.
```

solucion: 
```
frequency_is_c_over_lambda_ogfmaunraf
Nota:Flag is not in the usual flag format
```
## Notas adicionales
 **cifrado por sustitución** es un método de [cifrado](https://es.wikipedia.org/wiki/Cifrado_\(criptograf%C3%ADa\) "Cifrado (criptografía)") por el que unidades de texto plano son sustituidas con texto cifrado siguiendo un sistema regular; las "unidades" pueden ser una sola letra (el caso más común), pares de letras, tríos de letras, mezclas de lo anterior, entre otros. El receptor descifra el texto realizando la sustitución inversa.

Los cifrados por sustitución son comparables a los [cifrados por transposición](https://es.wikipedia.org/wiki/Cifrado_por_transposici%C3%B3n "Cifrado por transposición"). En un cifrado por transposición, las unidades del texto plano son cambiadas usando una ordenación diferente y normalmente bastante compleja, pero las unidades en sí mismas no son modificadas. Por el contrario, en un cifrado por sustitución, las unidades del texto plano mantienen el mismo orden, lo que hace es sustituir las propias unidades del texto plano.
## Referencias


