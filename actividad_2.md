# [diagrama de cuadros](https://miro.com/welcomeonboard/akh3eWRmcWl1N2tJUEdlSDZjenlrdmE2TkVMS3hQRmV5NkNBbUlGSXNhTURXUzhWTW43UWhxSnQzR05kWmlUQnwzNDU4NzY0NTk1OTA1NTc3NzA1fDI=?share_link_id=640780527382)

# ejercicios
## 1
### modulo de sensores

   - velosidad: 90 millas por hora
   - temperatura: -15°C
   - altitud: 5000

| 512 | 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |    datos    |
|-----|-----|-----|----|----|----|---|---|---|---|-------------|
|     |     |     |  1 |  0 |  1 | 1 | 0 | 1 | 0 |  velocidad  |
|     |     |     |    |    |  1 | 1 | 1 | 1 | 1 | temperatura |
|     |  1  |  1  |  1 |  1 |  1 | 0 | 1 | 0 | 0 |   altitud   |

temperatura: 
- 0000001111= 15
- 1111110001= -15

### modulo de codificacion
#### paridad 
    Paridad Par: En este caso, el bit de paridad se establece de manera que el número total de unos en el dato (incluyendo el bit de paridad) sea par. Si hay un número impar de unos, se agrega un uno al bit de paridad para que el total sea par

 - velocidad = 1011010**0**
 - temperatura = 1111110001**1**
 - altitud = 111110100**0** 

#### identificacion
|velocidad|temperatura|altitud|
|---------|-----------|-------|
|    00   |     10    |   01  |

 - velocidad= ~~00~~1011010**0**
 - temperatura = ~~10~~1111110001**1**
 - altitud = ~~01~~111110100**0** 
