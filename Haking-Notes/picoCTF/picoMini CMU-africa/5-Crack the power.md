### **Crack the power**

- **Descripción del Reto:** Se nos entrega un mensaje cifrado con RSA. El módulo `n` es muy grande, lo que hace inviable la factorización. La clave está en analizar los otros números proporcionados para encontrar una debilidad en el cifrado.
    
- **Procedimiento (Paso a Paso):**
    
    1. Analicé los datos proporcionados: un módulo `n` muy grande, un texto cifrado `c` y un exponente público `e`. Inmediatamente noté que el **exponente `e` era muy pequeño** (`e = 20`).
        
    2. Esta es una vulnerabilidad conocida en implementaciones débiles de RSA. Cuando `e` es pequeño, es posible que el mensaje original `m` elevado a la potencia `e` sea menor que el módulo `n` (es decir, `m^e < n`).
        
    3. Si la condición `m^e < n` se cumple, la operación de módulo en la fórmula de cifrado RSA (`c = m^e mod n`) no tiene efecto, simplificándose a `c = m^e`.
        
    4. Para descifrar el mensaje, solo necesitaba calcular la **raíz e-ésima** del texto cifrado `c`. En este caso, calculé la raíz 20 de `c`.
        
    5. Utilicé un script de Python con una biblioteca de alta precisión (como `gmpy2`) para calcular la raíz entera del número `c`.
        
        Python
        
        ```
        import gmpy2
        
        # Datos del reto
        c = 64063743081040685750056670209627407986808713193515305707898571646107848340979361580431188329659120332445224900845052103264526734551204676999438363528524438070515743262557006663252892531455290066981496321936933131315753460762035206131468349652588301684315324142577091170256338024730207374085082545237106327686761041472516465442130487307177423468322677764124009203252811604748913750737350006409994730452478289826566962868609140404409723579581865190202399690666812346537329222193413621695499921308685338047913660621403482703216221181191129945388455345988319278131933739198491295037127523237426211422070629507392434574310641341993171557020106707647127256173195950026227183784141730023055435959401842481386158948540051213150402736840026332185176203471959537973599912234032397327763823548261622540436321402776792299307534555920037483034551752944532847271306625743468413491387335958957641468179133317012304739086293363344011188339476043969815604827815461989578625957972779748806627496277469224410530886692336572296615503068103581450567422660534805519232388809973103168351180858136788457791131868302041724979040591162904501087765602504427166719596467074600
        e = 20
        
        # Calcular la raíz e-ésima de c
        m, exact = gmpy2.iroot(c, e)
        
        # Convertir el resultado de entero a texto
        flag_bytes = int(m).to_bytes((m.bit_length() + 7) // 8, 'big')
        flag = flag_bytes.decode('utf-8')
        ```
        
    6. El resultado del cálculo fue el mensaje `m` en formato numérico. Lo convertí a bytes y luego a texto (UTF-8) para obtener la bandera.
        
- **La Bandera:** `picoCTF{m4yb3_th4t_w4snt_s0_h4rd_1f3b3950}`