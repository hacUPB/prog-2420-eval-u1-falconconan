# preguntas
## partes del pc
1- escriba la diferencia entre un SSD y HDD 

2- ¿cual de las siguientes opciones es un dispositivo de entrada?

 - audifonos
 - impresora
 - microfono
 - SSD

## sistemas numeriocos
1- defina que es "overflow"

2- ¿cual es el numero mas grande en base decimal que se puede representar en 2 bytes?

## algoritmos
1- cuales son la principales caracteristicas de un algoritmo

2- **Gestión de Combustible en un Vuelo**

**Descripción:**

El objetivo es desarrollar un seudocódigo que gestione el combustible de un avión durante un vuelo. El programa deberá calcular la cantidad de combustible necesaria para un viaje, tomando en cuenta los kilómetros a volar, el consumo de combustible por kilómetro y la cantidad de combustible de reserva requerida. Además, antes de despegar, el programa revisará cuántos litros de combustible quedan del vuelo anterior y le pedirá al usuario que ingrese esa cantidad.

**Requerimientos:**

Declarar una variable de tipo entero para el resultado, inicializándola en cero.
Leer el valor devuelto por la función CalculaLitrosReserva() y asignarlo a una variable que dividirá el valor entero de litros.
Leer la variable que contiene el valor en kBPS de la charla previa para su procesamiento.

**Seudocódigo:**

```
Inicio
    Leer distancia_vuelo
    Leer consumo_por_km
    Leer combustible_reserva
    Leer combustible_disponible

    Calcular combustible_necesario = (distancia_vuelo * consumo_por_km) + combustible_reserva

    Si combustible_disponible >= combustible_necesario Entonces
        Escribir "El avión puede despegar."
    Sino
        Escribir "El avión no tiene suficiente combustible para el vuelo."
    FinSi
Fin
```