# problemas 
## problema 1
```
inicio

    leer #_calificaciones (#n)
    definir contador=#n
    definir suma_calificaciones=0
    definir promedio=0
    mientras contador>0 
        leer calificaciones (n)
            si n<0 y n>5 
                imprimir("nota no valida")
        suma_calificaciones=suma_calificaciones+n
        contador = contador-1
    fin mientras

    promedio=suma_calificaciones/#n
    imprimir promedio
fin
```
## problema 4
```
inicio
    definit distancia_total=0
    definit distancia_parcial=0
    leer #datos_velocidad(#DV)
    mientras #DV>0
        leer velocidad(v)
        leer tiempo(t)
            si t<0 y t>60
                imprimir "dato no valido"
        distancia_parcial=v*t
        distancia_total=distancia_total+distancia_parcial
        #DV=#DV-1
    fin mientras
    print mientras
fin
```
```
inicio
    definir distancia_total = 0
    leer #datos_velocidad (#DV)
    para i desde 1 hasta #DV hacer
        leer velocidad (v)
        leer tiempo (t)
        si t < 0 o t > 60 entonces
            imprimir "dato no valido"
        sino
            distancia_total = distancia_total + (v * t)
        fin si
    fin para
    imprimir distancia_total
fin
```
## problema 6

```
inicio
    Edad_Corregida=0
    Edad_No_Corregida=0
    leer año_nacimiento
    leer año_actual
    si año_nacimiento = año_actual
        imrpmir dato no valido
    si no 
        Edad_No_Corregida=año_actual-año_nacimiento
        leer Mes_De_Nacimiento
        leer Mes_Actual
            si Mes_De_Nacimiento>Mes_Actual
                Edad_Corregida=Edad_No_Corregida-1
            si Mes_De_Nacimiento<Mes_Actual
                Edad_Corregida=Edad_No_Corregida
            si Mes_De_Nacimiento=Mes_Actual
                leer Dia_De_Nacimiento
                leer Dia_Actual
                    si Dia_De_Nacimiento>Dia_Actual
                        Edad_Corregida=Edad_No_Corregida-1
                    si Dia_De_Nacimiento<Dia_Actual
                        Edad_Corregida=Edad_No_Corregida
                    si Dia_De_Nacimiento=Dia_Actual
                        imprimir "feliz cumpleaños"    
        imprimir Edad_Corregida
fin
```
