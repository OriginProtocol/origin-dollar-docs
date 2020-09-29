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

Para acuñar y quemar la cantidad apropiada de OUSD al entrar y salir, los contratos inteligentes deben fijar el precio con precisión del USDT, USDC y DAI que ingresa y sale del sistema. También necesita una forma confiable de expandir la oferta para distribuir el interés que se gana, o contratar la oferta si hay un cambio negativo en el valor de los activos subyacentes. Como protocolo descentralizado, OUSD debe depender de fuentes no centralizadas para estos precios.

{% hint style="info" %}
OUSD obtiene el precio de múltiples oráculos en cadena y usa el tipo de cambio que es más ventajoso para el grupo.
{% endhint %}

Con el fin de prevenir ataques maliciosos y alentar a los inversores a largo plazo sobre los especuladores a corto plazo, el contrato de OUSD compara las fuentes de precios de múltiples fuentes y utilizará el tipo de cambio que beneficie a todo el grupo sobre el individuo. Este mecanismo protege los fondos del grupo de liquidez de los arbitrajistas y evita que cualquier individuo pueda aprovechar cualquier ineficiencia temporal causada por oráculos mal valorados para agotar el grupo de liquidez de activos.

Esto protege los fondos en el grupo de liquidez mientras recompensa a los holders a largo plazo. Dado que el precio más seguro depende de la dirección de la operación, el oráculo de Origin expone tanto un `priceUSDMint ()` y un `priceUSDRedeem ()`. La función de reajuste utiliza `priceUSDMint ()` para mantener la coherencia.

Aquí está el conjunto inicial de oráculos que está siendo utilizado por OUSD:

{% embed url = "https://compound.finance/docs/prices" caption = ""%}

{% embed url = "https://feeds.chain.link/eth-usd" caption = ""%}

Se han implementado los siguientes oráculos, pero actualmente no se utilizan debido a los costos del gas:

{% embed url = "https://uniswap.org/docs/v2/core-concepts/oracles/" caption = ""%}

{% tabs %}
{% tab title = "DAI / USD"%}
Los siguientes oráculos se utilizan para obtener o calcular un precio de **DAI / USD:**

| Oráculo                  | Par         | Contrato                                     |
|:------------------------ |:----------- |:-------------------------------------------- |
| Feed de Precios Abiertos | DAI / USD   | 0xc629c26dced4277419cde234012f8160a0278a79   |
| Chainlink                | DAI / USD   | 0xa7D38FBD325a6467894A13EeFD977aFE558bC1f0   |
| Chainlink                | DAI / ETH   | 0x037E8F2125bF532F3e228991e051c8A7253B642c   |
| _Uniswap v2_             | _DAI / ETH_ | _0xA478c2975Ab1Ea89e8196811F51A7B7Ade33eB11_ |
{% endtab %}

{% tab title = "DAI / USD"%}
Los siguientes oráculos se utilizan para obtener o calcular un precio de **DAI / USD:**

| Oráculo                  | Par          | Contrato                                     |
|:------------------------ |:------------ |:-------------------------------------------- |
| Chainlink                | USDT / ETH   | 0xa874fe207DF445ff19E7482C746C4D3fD0CB9AcE   |
| Feed de Precios Abiertos | USDC / USD   | 0xc629c26dced4277419cde234012f8160a0278a79   |
| _Uniswap v2_             | _USDT / ETH_ | _0x0d4a11d5eeaac28ec3f61d100daf4d40471f1852_ |
{% endtab %}

{% tab title = "DAI / USD"%}
Los siguientes oráculos se utilizan para obtener o calcular un precio de **DAI / USD:**

| Oráculo                  | Par        | Contrato                                     |
|:------------------------ |:---------- |:-------------------------------------------- |
| Chainlink                | USDT / ETH | 0xdE54467873c3BCAA76421061036053e371721708   |
| Feed de Precios Abiertos | USDC / USD | 0xc629c26dced4277419cde234012f8160a0278a79   |
| _Uniswap v2_             | _USDC/ETH_ | _0xb4e16d0168e52d35cacd2c6185b44281ec28c9dc_ |
{% endtab %}

{% tab title="ETH/USD" %}
Since not all oracles have direct USD pairs, the protocol also fetches the prices for **ETH/USD** in order to calculate USD prices using ETH. Again, to be safe, the protocol chooses the most advantageous for the fund instead of the individual.

| Oracle          | Pair    | Contract                                   |
|:--------------- |:------- |:------------------------------------------ |
| Open Price Feed | ETH/USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| Chainlink       | ETH/USD | 0xF79D6aFBb6dA890132F9D7c355e3015f15F3406F |
{% endtab %}
{% endtabs %}

It is possible that additional oracles will be added to the protocol over time. Support may also be removed if any of these oracles become unreliable.

