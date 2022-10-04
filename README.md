# Estrategia de Regresion a la Media utilizando Bandas de Bollinger en temporalidad de 15 minutos para el par BTC/USD
Esta es una estrategia de comercio centrada en buscar la regresión a la media movil, utilizando Bandas de Bollinger para determinar cuando el precio esta lejos de la media, una SMA para determinar el Take Profit y el RSI para filtrar tendencias agresivas.

IMPORTANTE: ESTO NO ES UN CONSEJO FINANCIERO, USELA BAJO SU PROPIO RIESGO

# Bandas de Bollinger

Este indicador esta compuesto de la siguiente manera:

1) Media Movil (20 Periodos)
2) Banda Superior = Media Movil + 2 * Desviaciones Estandar
3) Banda Inferior = Media Movil - 2 * Desviaciones Estandar

Esto nos va a terminar creando un "canal" en el que se busca incluir el 95% de las cotizaciones

Se puede apreciar en el grafico de la siguiente manera:

![image](https://user-images.githubusercontent.com/99511913/193709042-4b812905-eccc-48a8-b594-cb388ab5a91b.png)

# RSI (Indice de Fuerza Relativo)

Se calcula con los siguientes elementos:

AvgU = promedio de las variaciones al alza del precio en el período N considerado.
AvgD = promedio de las variaciones a la baja del precio en el período N considerado.

FORMULA:
![image](https://user-images.githubusercontent.com/99511913/193709290-71bc616b-1586-4790-b65f-959e116832e4.png)

En el grafico se termina viendo como un Oscilador:

![image](https://user-images.githubusercontent.com/99511913/193710160-a0b68456-82f3-478a-a639-c808dcf77067.png)

Setearemos el mismo en 20 periodos y la zona en la que buscaremos operaciones se ubicara entre 35 y 65 puntos del Oscilador. 



# Reglas:

1) Se espera a que el precio salga de uno de los extremos del canal
2) En la 1era vela en que el precio de cierre este dentro del canal abriremos una posicion buscando la media como objetivo
3) Solo se operara cuando el RSI se encuentre entre los valores de 30 y 70 para filtrar tendencias fuertes.

# Stop Loss y Take Profit

SL: 1,5% fijo  
TP: Media Movil (20)  
NOTA: Podria considerar como un Segundo Take Profit la Banda Opuesta, sin embargo esto correra por su cuenta ya que no forma parte de la estrategia. 

# Ejemplo Operacion

![image](https://user-images.githubusercontent.com/99511913/193711150-c0fe85cc-b26c-4ea6-af73-a83e8063e590.png)

# Pruebas en los ultimos 2 meses en BTC/USD
Fuente de los datos historicos: Bitstamp.

  
IMPORTANTE: Esta muestra es demasiado chica, que los numeros den bien en un intervalo de 2 meses no significa que la estrategia sea rentable. Le recomiendo realizar un backtest de al menos 2-5 años y probarla en diferentes pares.
    
Cantidad de Operaciones de la muestra: 221    
Rentabilidad: 30%   
Profit Factor(Ganancias Totales / Perdidas Totales): 1.447    
Porcentaje de Operaciones Ganadoras: 73.76%   
Operacion Ganadora Promedio: 0.5%   
Operacion Perdedora Promedio: -0.94%    
Operacion Ganadora Promedio/Operacion Perdedora Promedio: 0.522   
Maxima Caida en la cuenta (Max Drawdown): -13.74%   



![image](https://user-images.githubusercontent.com/99511913/193711324-e6d178c5-f03b-41e1-941d-f8eafa6b23e2.png)



