- - -
descripción: OUSD usa Chainlink para proteger el protocolo de ataques de precios
- - -

# Precio de Oráculos

### Stablecoin Pricing

OUSD está diseñado para permanecer vinculado a 1 USD y tener un respaldo 1:1 con sus monedas estables subyacentes. Esto es más complicado de lo que parece porque estas monedas estables subyacentes se desvían constantemente de sus propias clavijas de 1 USD deseadas. Si bien la mayoría de las fluctuaciones diarias son menores, ha habido cambios importantes en el precio que se han producido en el pasado y es probable que vuelvan a ocurrir en el futuro.

| Moneda | **Bajo**                                             | **Alto**                                             | **Delta** | **Fuente**                                                                  |
| ------ | ---------------------------------------------------- | ---------------------------------------------------- | --------- | --------------------------------------------------------------------------- |
| USDC   | <p>$0.929222</p><p>13 de marzo de 2020</p>   | <p>1,11 USD</p><p>15 de octubre de 2018</p>   | $0.180778 | [CoinMarketCap](https://coinmarketcap.com/currencies/usd-coin/)             |
| USDC   | <p>$0.924188</p><p>02 de agosto de 2020</p>   | <p>1,17 USD</p><p>08 de mayo de 2019</p>   | $0.245812 | [CoinGecko](https://www.coingecko.com/en/coins/usd-coin)                    |
| DAI    | <p>$0.945505</p><p>10 de mayo de 2020</p>   | <p>1,11 USD</p><p>13 de marzo de 2020</p> | $0.164495 | [CoinMarketCap](https://coinmarketcap.com/currencies/multi-collateral-dai/) |
| DAI    | <p>$0.903243</p><p>25 de noviembre de 2019</p> | <p>1.22 USD</p><p>13 de marzo de 2020</p> | $0.316757 | [CoinGecko](https://www.coingecko.com/en/coins/dai)                         |
| USDT   | <p>$0.849809</p><p>02 de febrero de 2017</p> | <p>1.21 USD</p><p>27 de mayo de 2017</p> | $0.360191 | [CoinGecko](https://www.coingecko.com/en/coins/tether)                      |
| USDT   | <p>$0.572521</p><p>02 de marzo de 2015</p> | <p>1.32 USD</p><p>24 de julio de 2018</p> | $0,747479 | [CoinMarketCap](https://coinmarketcap.com/currencies/tether/)               |

La función de rebase trata 1 moneda estable como 1 OUSD por simplicidad y para proteger los saldos de OUSD de verse afectados por las fluctuaciones diarias en el precio de las monedas estables subyacentes. Since the rebase function only counts coins, OUSD balances should only increase.&#x20;

In order to mint and redeem the appropriate number of OUSD on entry and exit, the smart contracts need to accurately price the USDT, USDC, and DAI that is entering and exiting the system.&#x20;

As an added precaution, OUSD never pays more than a dollar for a stablecoin, nor sells a stablecoin for less than a dollar. Oracles giving wrong prices will not result in a reduction of the number of stablecoins held. Gains that are collected as a result of stablecoins slipping from their peg are redistributed to the remaining holders of OUSD in the form of additional yield.

Como protocolo descentralizado, OUSD debe depender de fuentes no centralizadas para estos precios. OUSD usa Chainlink como oráculo para DAI, USDC y USDT. Puede [leer más sobre nuestra decisión de trabajar con Chainlink](https://blog.originprotocol.com/how-origin-uses-chainlink-oracles-to-secure-ousd-bff5601e840e) en el blog de Origin. Here are the Chainlink oracles we are currently using for stablecoin pricing:

{% embed url="https://data.chain.link/usdt-usd"%}

{% embed url="https://data.chain.link/usdc-usd"%}

{% embed url="https://data.chain.link/dai-usd"%}

### Reward Token Oracles & Front Running Protection

When reward tokens from OUSD strategies are sold for additional yield, Chainlink oracles are checked to ensure that the sale price slippage has not exceeded normal bounds. These oracles are listed on our [registry](../smart-contracts/registry.md) page under the "Oracles" tab.

The same is also true for OGN buybacks from OUSD yield.\ \ When minting and redeeming OUSD, a miniumun required amount can be passed into the contract call to ensure that the entire transaction fails if not enough OUSD or stablecoins would be returned to the user due to changing prices.
