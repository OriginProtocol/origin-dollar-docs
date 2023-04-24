# Precio de Oráculos

OUSD está diseñado para mantenerse vinculado a 1 USD y tener un respaldo 1:1 con sus monedas estables subyacentes. Esto es más complicado de lo que parece porque estas monedas estables subyacentes se desvían constantemente de sus propias clavijas de 1 USD deseadas. Si bien la mayoría de las fluctuaciones diarias son menores, ha habido cambios importantes en el precio que se han producido en el pasado y es probable que vuelvan a ocurrir en el futuro.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Moneda</th>
      <th style="text-align:left"><b>Bajo</b>
      </th>
      <th style="text-align:left"><b>Alto</b>
      </th>
      <th style="text-align:left"><b>Delta</b>
      </th>
      <th style="text-align:left"><b>Fuente</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$0.929222</p>
        <p>13 de marzo de 2020</p>
      </td>
      <td style="text-align:left">
        <p>1,11 USD</p>
        <p>15 de octubre de 2018</p>
      </td>
      <td style="text-align:left">$0.180778</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$0.924188</p>
        <p>02 de agosto de 2020</p>
      </td>
      <td style="text-align:left">
        <p>1,17 USD</p>
        <p>08 de mayo de 2019</p>
      </td>
      <td style="text-align:left">$0.245812</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$0.945505</p>
        <p>10 de mayo de 2020</p>
      </td>
      <td style="text-align:left">
        <p>1,11 USD</p>
        <p>13 de marzo de 2020</p>
      </td>
      <td style="text-align:left">$0.164495</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$0.903243</p>
        <p>25 de noviembre de 2019</p>
      </td>
      <td style="text-align:left">
        <p>1.22 USD</p>
        <p>13 de marzo de 2020</p>
      </td>
      <td style="text-align:left">$0.316757</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$0.849809</p>
        <p>02 de febrero de 2017</p>
      </td>
      <td style="text-align:left">
        <p>1.21 USD</p>
        <p>27 de mayo de 2017</p>
      </td>
      <td style="text-align:left">$0.360191</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$0.572521</p>
        <p>02 de marzo de 2015</p>
      </td>
      <td style="text-align:left">
        <p>1.32 USD</p>
        <p>24 de julio de 2018</p>
      </td>
      <td style="text-align:left">$0,747479</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/tether/">CoinMarketCap</a>
      </td>
    </tr>
  </tbody>
</table>

La función de rebase trata 1 moneda estable como 1 OUSD por simplicidad y para proteger los saldos de OUSD de verse afectados por las fluctuaciones diarias en el precio de las monedas estables subyacentes. Dado que la función de rebase solo cuenta monedas, los saldos de OUSD solo deberían aumentar.

Para acuñar y quemar la cantidad apropiada de OUSD al entrar y salir, los contratos inteligentes deben fijar el precio con precisión del USDT, USDC y DAI que ingresa y sale del sistema. Como protocolo descentralizado, OUSD debe depender de fuentes no centralizadas para estos precios.

{% hint style="info" %}
OUSD obtiene el precio de múltiples oráculos en cadena y usa el tipo de cambio que es más ventajoso para el grupo.
{% endhint %}

Con el fin de prevenir ataques maliciosos y alentar a los inversores a largo plazo sobre los especuladores a corto plazo, el contrato de OUSD compara las fuentes de precios de múltiples fuentes y utilizará el tipo de cambio que beneficie a todo el grupo sobre el individuo. Este mecanismo protege los fondos del grupo de liquidez de los arbitrajistas y evita que cualquier individuo pueda aprovechar cualquier ineficiencia temporal causada por oráculos mal valorados para agotar el grupo de liquidez de activos.

Esto protege los fondos en el grupo de liquidez mientras recompensa a los holders a largo plazo. Dado que el precio más seguro depende de la dirección de la operación, el oráculo de Origin expone tanto un `priceUSDMint()` y un `priceUSDRedeem()`.

OUSD usa Chainlink como oráculo para DAI, USDC y USDT.

{% embed url="https://feeds.chain.link/eth-usd" caption=""%}

La dirección de contrato inteligente específica para cada oráculo que se utiliza se enumera en nuestra [página de registro](../../smart-contracts/registry.md).

Es posible que con el tiempo se agreguen más oráculos al protocolo. También pueden eliminarse si alguno de estos oráculos deja de ser confiable.

