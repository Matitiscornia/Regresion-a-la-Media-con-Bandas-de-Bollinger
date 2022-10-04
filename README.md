# Estrategia de Regresion a la Media utilizando Bandas de Bollinger 
Esta es una estrategia centrada de comercio centrada en buscar una regresión a la media movil, utilizando Bandas de Bollinger para determinar cuando el precio esta muy alejado de la misma, y el RSI para filtrar tendencias agresivas.


# Reglas:

1) Se espera a que el precio salga de uno de los extremos del canal
2) En la 1era vela en que se vuelva a entrar abrimos una posicion buscando la media como objetivo
3) Solo se operara cuando el RSI se encuentre entre los valores de 30 y 70 para filtrar tendencias fuertes.

