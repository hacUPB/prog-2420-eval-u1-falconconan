# [diagrama de bloques](https://miro.com/welcomeonboard/akh3eWRmcWl1N2tJUEdlSDZjenlrdmE2TkVMS3hQRmV5NkNBbUlGSXNhTURXUzhWTW43UWhxSnQzR05kWmlUQnwzNDU4NzY0NTk1OTA1NTc3NzA1fDI=?share_link_id=640780527382)

# ejercicios
## modulo de sensores

- velosidad: 
   - 90 
   - 120
   - 240
- temperatura: 
   - -15
   - -2
   - 50
- altitud: 
   - 25000
   - 40000
   - 35000

|4096|2048|1024| 512 | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |    datos    |
|----|----|----|-----|-----|-----|----|----|----|---|---|---|---|-------------|
|    |    |    |     |     |     |  1 |  0 |  1 | 1 | 0 | 1 | 0 |  velocidad  |
|    |    |    |     |     |     |  1 |  1 |  1 | 1 | 0 | 0 | 0 |      "      |
|    |    |    |     |     |  1  |  1 |  1 |  1 | 0 | 0 | 0 | 0 |      "      |
|    |    |    |     |     |     |    |    |  1 | 1 | 1 | 1 | 1 | temperatura |
|    |    |    |     |     |     |    |    |    |   |   | 1 | 0 |      "      |
|    |    |    |     |     |     |    |  1 |  1 | 0 | 0 | 1 | 0 |      "      |
|    |  1 |  0 |  0  |  1  |  1  |  1 |  0 |  0 | 0 | 1 | 0 | 0 |   altitud   |
|    |  1 |  1 |   1 |  1  |  1  |  0 |  1 |  0 | 0 | 0 | 0 | 0 |      "      |
|    |  1 |  1 |   0 |  1  |  1  |  0 |  1 |  0 | 1 | 1 | 0 | 0 |      "      |

temperatura: complemento A2
 - 0000001111= 15
   - 1111110001= -15
 - 0000000010= 2
   - 1111111110= -2

## modulo de codificacion

### paridad 
   - _**Paridad Par**_: En este caso, el bit de paridad se establece de manera que el número total de unos en el dato (incluyendo el bit de paridad) sea par. Si hay un número impar de unos, se agrega un uno al bit de paridad para que el total sea par

- velocidad:
  - 0000001011010**0**
  - 0000001111000**0**
  - 0000011110000**0**
- temperatura:
  - 1111111110001**1**
  - 1111111111110**1**
  - 0000000110010**1**
- altitud: 
  - 0100111000100**0** 
  - 0111110100000**0**
  - 0110110101100**1**

### identificacion
|velocidad|temperatura|altitud|
|---------|-----------|-------|
|    00   |     10    |   01  |

 - velocidad:
   - ~~00~~0000001011010**0**
   - ~~00~~0000001111000**0**
   - ~~00~~0000011110000**0**

 - temperatura:
   - ~~10~~1111111110001**1**
   - ~~10~~1111111111110**1**
   - ~~10~~0000000110010**1**

 - altitud:
   - ~~01~~0100111000100**0**
   - ~~01~~0111110100000**0**
   - ~~01~~0110110101100**1**

Nota: todos los datos estan trabajando en 16 byts

## Módulo de Conversión Bin2Dec:

|8192|4096|2048|1024| 512 | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|----|----|----|----|-----|-----|-----|----|----|----|---|---|---|---|
|    |    |    |    |     |     |     |  1 |  0 |  1 | 1 | 0 | 1 | 0 |
|    |    |    |    |     |     |     |  1 |  1 |  1 | 1 | 0 | 0 | 0 |
|    |    |    |    |     |     |  1  |  1 |  1 |  1 | 0 | 0 | 0 | 0 |
|    |  1 |  1 |  1 |  1  |  1  |  1  |  1 |  1 |  0 | 0 | 0 | 0 | 1 |
|    |  1 |  1 |  1 |  1  |  1  |  1  |  1 |  1 |  1 | 1 | 1 | 1 | 0 |
|    |    |    |    |     |     |     |    |  1 |  1 | 0 | 0 | 1 | 0 |
|    |    |  1 |  0 |  0  |  1  |  1  |  1 |  0 |  0 | 0 | 1 | 0 | 0 |
|    |    |  1 |  1 |  1  |  1  |  1  |  0 |  1 |  0 | 0 | 0 | 0 | 0 |
|    |    |  1 |  1 |  0  |  1  |  1  |  0 |  1 |  0 | 1 | 1 | 0 | 0 |


   - ~~00~~0000001011010**0**
   - ~~00~~0000001111000**0**
   - ~~00~~0000011110000**0**
   - ~~10~~1111111110001**1**
   - ~~10~~1111111111110**1**
   - ~~10~~0000000110010**1**
   - ~~01~~0100111000100**0**
   - ~~01~~0111110100000**0**
   - ~~01~~0110110101100**1**


- velosidad: 
   - 90 
   - 120
   - 240
- temperatura: 
   - -15
   - -2
   - 50
- altitud: 
   - 25000
   - 40000
   - 35000

## Módulo de Cálculo de Error:
$Error=Valor_{Medido}-SetPoint$

### velocidad
- $SetPoint$ = 150
   - 90 
   - 120
   - 240

- $ERROR$= 90-150= -60
- $ERROR$= 120-150= -30
- $ERROR$= 240-150= 90

### temperatura
- $SetPoint$ = 11
   - -15
   - -2
   - 50

- $ERROR$= -15-11= -26
- $ERROR$= -2-11= -13
- $ERROR$= 50-11= 39

### altitud
- $SetPoint$ = 27000
   - 25000
   - 40000
   - 35000

- $ERROR$= 25000-27000 
  = -2000
- $ERROR$= 40000-27000 
 = 13000
- $ERROR$= 35000-27000
= 8000

## Módulo de Control
$Control = Error * K_P$

### velocidad
$k_p$=10

- $ERROR$= -60
- $ERROR$= -30
- $ERROR$= 90
  - $Control$= -60*10= -600
  - $Control$= -30*10= -300
  - $Control$= 90*10= 900

### temperatura
$k_p$=15

- $ERROR$= -26
- $ERROR$= -13
- $ERROR$= 39
  - $Control$= -26*15= -390
  - $Control$= -13*15=-195
  - $Control$= 39*15= 585

### altitud
$k_p$=9

- $ERROR$= -2000
- $ERROR$= 13000
- $ERROR$= 8000
  - $Control$= -2000*9= 18000
  - $Control$= 13000*9= 117000
  - $Control$= 8000*9= 72000

## Módulo de Codificación de la CPU:

### velocidad
  - $Control$= -600
  - $Control$= -300
  - $Control$= 900

|8192|4096|2048|1024| 512 | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|----|----|----|----|-----|-----|-----|----|----|----|---|---|---|---|
|    |    |    |    |  1  |  0  |  0  |  1 |  0 |  1 | 1 | 0 | 0 | 0 |
|    |    |    |    |     |  1  |  0  |  0 |  1 |  0 | 1 | 1 | 0 | 0 |
|    |    |    |    |  1  |  1  |  1  |  0 |  0 |  0 | 0 | 1 | 0 | 0 |

  - 600= ~~00~~00001001011000
    - -600= ~~00~~11110110101000
  - 300= ~~00~~00000100101100
    - -300= ~~00~~11111011010100 
  - 900= ~~00~~00001110000100 
### temperatura

  - $Control$= -390
  - $Control$=-195
  - $Control$= 585

| 8192 | 4096 | 2048 | 1024 | 512 | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|------|------|------|------|-----|-----|-----|----|----|----|---|---|---|---|
|      |      |      |      |     |  1  |  1  |  0 |  0 |  0 | 0 | 1 | 1 | 0 |
|      |      |      |      |     |     |  1  |  1 |  0 |  0 | 0 | 0 | 1 | 1 |
|      |      |      |      |  1  |  0  |  0  |  1 |  0 |  0 | 1 | 0 | 0 | 1 |


- 390= ~~01~~00000110010000
  - -390=~~01~~11111001110000
- 195= ~~01~~00000011000011
  - -195= ~~01~~11111100111100
- 585= ~~01~~00001001001001

### altitud

  - $Control$= -18000 = ~~10~~111011100110110000
  - $Control$= 117000 = ~~10~~011100100100001000
  - $Control$= 72000  = ~~10~~010001100101000000

## concluciones

1. **Eficiencia en la Codificación y Decodificación**:
   - La correcta codificación y decodificación de los datos de los sensores es crucial para asegurar la integridad de la información transmitida. Utilizar bits de encabezado para identificar el sensor y agregar un bit de paridad para el control de errores garantiza que los datos sean precisos y confiables al llegar a su destino.

2. **Precisión en la Conversión y Cálculo de Errores**:
   - La conversión de datos binarios a decimales y hexadecimales permite una interpretación más fácil y precisa de las variables medidas. Además, calcular el error comparando los valores medidos con los valores de referencia (Set Point) es esencial para identificar desviaciones y ajustar el sistema de control de manera adecuada.

3. **Control Proporcional Efectivo**:
   - Aplicar un control proporcional a los valores de error mediante la multiplicación por una constante ($K_P$) permite ajustar las variables de manera eficiente. Este enfoque ayuda a mantener las variables dentro de los rangos deseados, asegurando un funcionamiento óptimo del sistema de control de la aeronave.

