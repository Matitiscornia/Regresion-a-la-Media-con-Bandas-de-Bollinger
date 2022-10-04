# Estrategia de Regresion a la Media utilizando Bandas de Bollinger 
Esta es una estrategia de comercio centrada en buscar la regresión a la media movil, utilizando Bandas de Bollinger para determinar cuando el precio esta lejos de la media, una SMA para determinar el Take Profit y el RSI para filtrar tendencias agresivas.

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

En el grafico se termina viendo como un Oscilador:

![image](https://user-images.githubusercontent.com/99511913/193709290-71bc616b-1586-4790-b65f-959e116832e4.png)



# Reglas:

1) Se espera a que el precio salga de uno de los extremos del canal
2) En la 1era vela en que se vuelva a entrar abrimos una posicion buscando la media como objetivo
3) Solo se operara cuando el RSI se encuentre entre los valores de 30 y 70 para filtrar tendencias fuertes.

# Stop Loss y Take Profit

SL: 1,5% fijo  
TP: Media Movil (20)  
NOTA: Podria considerar como un Segundo Take Profit la Banda Opuesta, sin embargo esto correra por su cuenta ya que no forma parte de la estrategia. 
