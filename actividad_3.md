# problemas 
## problema 1
```
inicio

    leer N_calificaciones (Nc)
    definir contador=Nc
    definir suma_calificaciones=0
    definir promedio=0
    mientras contador>0 
        leer calificaciones (n)
            si n<0 y n>5 
                imprimir("nota no valida")
        suma_calificaciones=suma_calificaciones+n
        contador = contador-1
    fin mientras

    promedio=suma_calificaciones/Nc
    imprimir promedio
fin
```
## problema 4
```
inicio
    definit distancia_total=0
    definit distancia_parcial=0
    leer N_datos_velocidad(Ndv)
    mientras Ndv>0
        leer velocidad(v)
        leer tiempo(t)
            si t<0 y t>60
                imprimir "dato no valido"
        distancia_parcial=v*t
        distancia_total=distancia_total+distancia_parcial
        Ndv=Ndv-1
    fin mientras
    print mientras
fin
```
```
inicio
    definir distancia_total = 0
    leer N_datos_velocidad (Ndv)
    para i desde 1 hasta Ndv hacer
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
            fin si

            si Mes_De_Nacimiento<Mes_Actual
                Edad_Corregida=Edad_No_Corregida
            fin si

            si Mes_De_Nacimiento=Mes_Actual
                leer Dia_De_Nacimiento
                leer Dia_Actual

                    si Dia_De_Nacimiento>Dia_Actual
                        Edad_Corregida=Edad_No_Corregida-1
                    fin si

                    si Dia_De_Nacimiento<Dia_Actual
                        Edad_Corregida=Edad_No_Corregida
                    fin si
                    
                    si Dia_De_Nacimiento=Dia_Actual
                        imprimir "feliz cumpleaños"
                    fin si
            fin si
    fin si 
        imprimir Edad_Corregida
fin
```
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
        si no
            si Mes_De_Nacimiento<Mes_Actual
                Edad_Corregida=Edad_No_Corregida
            si no
                leer Dia_De_Nacimiento
                leer Dia_Actual
                si Dia_De_Nacimiento>Dia_Actual
                    Edad_Corregida=Edad_No_Corregida-1
                si no
                    si Dia_De_Nacimiento<Dia_Actual
                        Edad_Corregida=Edad_No_Corregida
                    si no
                        imprimir "feliz cumpleaños"
                    fin si
                fin si
            fin si
        fin si
    fin si 
    imprimir Edad_Corregida
fin
```
## ejescicio de clase

```
inicio
//print ("hellow world")
    definir costo=0
    leer N_Horas (NH)
    si NH>10 
       costo=NH*2
    si no
        si 0<NH<=2
            costo=5*NH
        si no
            si NH<=5
                costo=(5*2)+(4*(NH-2))
            si no 
                costo=(5*2)+(4*3)+(3*(NH-5))
            fin si
        fin si
    fin si
print costo
fin
````

## ejercicio targeta credito
