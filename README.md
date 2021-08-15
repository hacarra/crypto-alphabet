# crypto-alphabet

Jupyter script para pronosticar el precio de cierre de Bitcoin y Ethereum usando [Prophet](https://facebook.github.io/prophet/) de Facebook.

Basado en el [trabajo de](https://medium.com/jake404/predict-the-price-of-btc-using-facebook-prophet-8b5e22f669aa) [Jacob Bennett](https://go.jake404.com)  

Los datos se obtienen desde la API de http://poloniex.com

https://poloniex.com/public?command=returnChartData&currencyPair=USDT_ETH&start=1435699200&end=9999999999&period=14400
https://poloniex.com/public?command=returnChartData&currencyPair=USDT_BTC&start=1435699200&end=9999999999&period=14400


Después de descargar el dataset, se debe transformar el timestamp a fecha. Yo usé excel con esta fórmula en PowerQuery ==> Table.AddColumn(#"Expanded Column1", "DateTime", each #datetime(1970,1,1,0,0,0) + #duration(0,0,0,[Column1.date]))

## Ethereum

### Forecast
![image](https://user-images.githubusercontent.com/47190969/129463291-cfd51899-8466-4624-97d2-072fe7cc5f40.png)

### Componentes
![image](https://user-images.githubusercontent.com/47190969/129463293-46ed90d5-7349-487f-824b-0483f01a8c82.png)

## BitCoin
### Forecast
![image](https://user-images.githubusercontent.com/47190969/129463296-14188ba0-1ea9-45d6-8ff6-27c5e3a4b0eb.png)

### Componentes
![image](https://user-images.githubusercontent.com/47190969/129463301-7c467877-131e-45a0-b5c0-036482464ee2.png)

