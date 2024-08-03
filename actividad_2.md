# [diagrama de boques](https://miro.com/welcomeonboard/akh3eWRmcWl1N2tJUEdlSDZjenlrdmE2TkVMS3hQRmV5NkNBbUlGSXNhTURXUzhWTW43UWhxSnQzR05kWmlUQnwzNDU4NzY0NTk1OTA1NTc3NzA1fDI=?share_link_id=640780527382)

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
   - 5000
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
|    |    |    |     |  1  |  1  |  1 |  1 |  1 | 0 | 1 | 0 | 0 |   altitud   |
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
  - 0000111110100**0** 
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
   - ~~01~~0000111110100**0**
   - ~~01~~0111110100000**0**
   - ~~01~~0110110101100**1**

Nota: todos los datos estan trabajando en 16 byts

## Módulo de Conversión Bin2Dec:

|4096|2048|1024| 512 | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|----|----|----|-----|-----|-----|----|----|----|---|---|---|---|
|    |    |    |     |     |     |  1 |  0 |  1 | 1 | 0 | 1 | 0 |
|    |    |    |     |     |     |  1 |  1 |  1 | 1 | 0 | 0 | 0 |
|    |    |    |     |     |  1  |  1 |  1 |  1 | 0 | 0 | 0 | 0 |
|  1 |  1 |  1 |  1  |  1  |  1  |  1 |  1 |  0 | 0 | 0 | 0 | 1 |
|  1 |  1 |  1 |  1  |  1  |  1  |  1 |  1 |  1 | 1 | 1 | 1 | 0 |
|    |    |    |     |     |     |    |  1 |  1 | 0 | 0 | 1 | 0 |
|    |    |    |     |  1  |  1  |  1 |  1 |  1 | 0 | 1 | 0 | 0 |
|    |  1 |  1 |  1  |  1  |  1  |  0 |  1 |  0 | 0 | 0 | 0 | 0 |
|    |  1 |  1 |  0  |  1  |  1  |  0 |  1 |  0 | 1 | 1 | 0 | 0 |


   - ~~00~~0000001011010**0**
   - ~~00~~0000001111000**0**
   - ~~00~~0000011110000**0**
   - ~~10~~1111111110001**1**
   - ~~10~~1111111111110**1**
   - ~~10~~0000000110010**1**
   - ~~01~~0000111110100**0**
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
   - 5000
   - 40000
   - 35000

## Módulo de Cálculo de Error:
  $Error=Valor_{Medido}-SetPoint$

- $SetPoint$ = 