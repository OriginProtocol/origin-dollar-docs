- - -
descripción: OUSD usa Chainlink para proteger el protocolo de ataques de precios
- - -

# Precio de Oráculos

OUSD está diseñado para permanecer vinculado a 1 USD y tener un respaldo 1:1 con sus monedas estables subyacentes. Esto es más complicado de lo que parece porque estas monedas estables subyacentes se desvían constantemente de sus propias clavijas de 1 USD deseadas. Si bien la mayoría de las fluctuaciones diarias son menores, ha habido cambios importantes en el precio que se han producido en el pasado y es probable que vuelvan a ocurrir en el futuro.

| Moneda | **Bajo**                                             | **Alto**                                             | **Delta** | **Fuente**                                                                  |
| ------ | ---------------------------------------------------- | ---------------------------------------------------- | --------- | --------------------------------------------------------------------------- |
| USDC   | <p>$0.929222</p><p>13 de marzo de 2020</p>   | <p>1,11 USD</p><p>15 de octubre de 2018</p>   | $0.180778 | [CoinMarketCap](https://coinmarketcap.com/currencies/usd-coin/)             |
| USDC   | <p>$0.924188</p><p>02 de agosto de 2020</p>   | <p>1,17 USD</p><p>08 de mayo de 2019</p>   | $0.245812 | [CoinGecko](https://www.coingecko.com/en/coins/usd-coin)                    |
| DAI    | <p>$0.945505</p><p>10 de mayo de 2020</p>   | <p>1,11 USD</p><p>13 de marzo de 2020</p> | $0.164495 | [CoinMarketCap](https://coinmarketcap.com/currencies/multi-collateral-dai/) |
| DAI    | <p>$0.903243</p><p>25 de noviembre de 2019</p> | <p>1.22 USD</p><p>13 de marzo de 2020</p> | $0.316757 | [CoinGecko](https://www.coingecko.com/en/coins/dai)                         |
| USDT   | <p>$0.849809</p><p>02 de febrero de 2017</p> | <p>1.21 USD</p><p>27 de mayo de 2017</p> | $0.360191 | [CoinGecko](https://www.coingecko.com/en/coins/tether)                      |
| USDT   | <p>$0.572521</p><p>02 de marzo de 2015</p> | <p>1.32 USD</p><p>24 de julio de 2018</p> | $0,747479 | [CoinMarketCap](https://coinmarketcap.com/currencies/tether/)               |

La función de rebase trata 1 moneda estable como 1 OUSD por simplicidad y para proteger los saldos de OUSD de verse afectados por las fluctuaciones diarias en el precio de las monedas estables subyacentes. Dado que la función de rebase solo cuenta monedas, los saldos de OUSD solo deberían aumentar.

Para acuñar y quemar la cantidad apropiada de OUSD al entrar y salir, los contratos inteligentes deben fijar el precio con precisión del USDT, USDC y DAI que ingresa y sale del sistema.

Como precaución adicional, OUSD nunca paga más de un dólar por una moneda estable. Esto evita que el protocolo sea atacado a través de oráculos con precios incorrectos. Cualquier ganancia adicional que se recolecte como resultado de que las monedas estables se salgan de su paridad se redistribuye a los holders restantes de OUSD en forma de rendimiento adicional.

Como protocolo descentralizado, OUSD debe depender de fuentes no centralizadas para estos precios. OUSD usa Chainlink como oráculo para DAI, USDC y USDT. Puede [leer más sobre nuestra decisión de trabajar con Chainlink](https://blog.originprotocol.com/how-origin-uses-chainlink-oracles-to-secure-ousd-bff5601e840e) en el blog de Origin. Aquí están los oráculos Chainlink que estamos usando actualmente:

{% embed url="https://data.chain.link/usdt-usd"%}

{% embed url="https://data.chain.link/usdc-usd"%}

{% embed url="https://data.chain.link/dai-usd"%}

La dirección de contrato inteligente específica para cada oráculo que se utiliza se enumera en nuestra [página de registro](../smart-contracts/registry.md). Es posible que con el tiempo se agreguen más oráculos al protocolo. También pueden eliminarse si alguno de estos oráculos deja de ser confiable.
