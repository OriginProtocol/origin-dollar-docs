# Ценовые оракулы

OUSD рассчитан на то, чтобы оставаться привязанным к 1 доллару США и быть обеспеченным базовыми стейблкоинами в соотношении 1:1. Это сложнее, чем кажется, потому что эти базовые стейблкоины постоянно отклоняются от своих желаемых привязок к 1 доллару США. Большинство дневных колебаний незначительны, однако в прошлом были серьезные колебания цен, которые, вероятно, повторятся и в будущем.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Монета</th>
      <th style="text-align:left"><b>Низкий</b>
      </th>
      <th style="text-align:left"><b>Высокий</b>
      </th>
      <th style="text-align:left"><b>Разница</b>
      </th>
      <th style="text-align:left"><b>Источник</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$0,929222</p>
        <p>13 марта 2020 г.</p>
      </td>
      <td style="text-align:left">
        <p>$ 1,11</p>
        <p>15 октября 2018 г.</p>
      </td>
      <td style="text-align:left">$0.180778</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$0.924188</p>
        <p>2 августа 2020 г.</p>
      </td>
      <td style="text-align:left">
        <p>$1.17</p>
        <p>8 мая 2019г.</p>
      </td>
      <td style="text-align:left">$0.245812</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$0.945505</p>
        <p>10 мая 2020г.</p>
      </td>
      <td style="text-align:left">
        <p>$1.11</p>
        <p>13 марта 2020г.</p>
      </td>
      <td style="text-align:left">$0.164495</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$0.903243</p>
        <p>25 ноября 2019г.</p>
      </td>
      <td style="text-align:left">
        <p>$1.22</p>
        <p>13 марта 2020г.</p>
      </td>
      <td style="text-align:left">$0.316757</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$0,849809</p>
        <p>2 февраля 2017г.</p>
      </td>
      <td style="text-align:left">
        <p>$1.21</p>
        <p>27 мая 2017г.</p>
      </td>
      <td style="text-align:left">$0.360191</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$0.572521</p>
        <p>02 марта 2015г.</p>
      </td>
      <td style="text-align:left">
        <p>$1.32</p>
        <p>24 июля 2018г.</p>
      </td>
      <td style="text-align:left">$0.747479</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/tether/">CoinMarketCap</a>
      </td>
    </tr>
  </tbody>
</table>

Чтобы создать и сжечь соответствующее количество OUSD при входе и выходе, смарт-контракты должны точно определять цену на USDT, USDC и DAI, которые входят в систему и выходят из нее. Также необходим надежный способ увеличения предложения для распределения заработанных процентов или предложения по контрактам, если есть отрицательное изменение стоимости базовых активов. Как децентрализованный протокол, OUSD должен полагаться на децентрализованные источники этих цен.

{% hint style="info" %}
OUSD получает цену от нескольких оракулов в сети и использует обменный курс, который является наиболее выгодным для пула.
{% endhint %}

Чтобы предотвратить злонамеренные атаки и больше поощрять долгосрочных инвесторов, чем краткосрочных спекулянтов, контракт OUSD сравнивает потоки цен из нескольких источников и использует тот обменный курс, который выгоден для всего пула, а не для отдельных лиц. Этот механизм защищает средства пула от арбитражеров и никому не позволяет воспользоваться любой временной неэффективностью, вызванной ошибкой оракулов, для истощения общего пула активов.

Это защищает средства в пуле и поощряет долгосрочных держателей. Поскольку самая безопасная цена зависит от направления сделки, оракул Origin предоставляет как `priceUSDMint ()`, так и `priceUSDRedeem ()`. Функция перебалансировки использует `priceUSDMint ()` для согласованности.

OUSD изначально использует следующий набор оракулов:

{% embed url="https://compound.finance/docs/prices" caption="" %}

{% embed url="https://feeds.chain.link/eth-usd" caption="" %}

Следующие оракулы были реализованы, но в настоящее время не используются из-за больших затрат на газ:

{% embed url="https://uniswap.org/docs/v2/core-concepts/oracles/" caption="" %}

{% tabs %}
{% tab title="DAI/USD" %}
Следующие оракулы используются для получения или вычисления цены **DAI / USD:**

| Оракул          | Пара      | Контракт                                     |
|:--------------- |:--------- |:-------------------------------------------- |
| Open Price Feed | DAI/USD   | 0xc629c26dced4277419cde234012f8160a0278a79   |
| Chainlink       | DAI/USD   | 0xa7D38FBD325a6467894A13EeFD977aFE558bC1f0   |
| Chainlink       | DAI/ETH   | 0x037E8F2125bF532F3e228991e051c8A7253B642c   |
| _Uniswap v2_    | _DAI/ETH_ | _0xA478c2975Ab1Ea89e8196811F51A7B7Ade33eB11_ |
{% endtab %}

{% tab title="USDT/USD" %}
Следующие оракулы используются для извлечения или вычисления цены **DAI/USD:**

| **Оракул**      | Пара       | Контракт                                     |
|:--------------- |:---------- |:-------------------------------------------- |
| Chainlink       | USDT/ETH   | 0xa874fe207DF445ff19E7482C746C4D3fD0CB9AcE   |
| Open Price Feed | USDC/USD   | 0xc629c26dced4277419cde234012f8160a0278a79   |
| _Uniswap v2_    | _USDT/ETH_ | _0x0d4a11d5eeaac28ec3f61d100daf4d40471f1852_ |
{% endtab %}

{% tab title="USDC/USD" %}
Следующие оракулы используются для извлечения или вычисления цены **USDC/USD:**

| **Оракул**      | Пара       | Контракт                                     |
|:--------------- |:---------- |:-------------------------------------------- |
| Chainlink       | USDC/ETH   | 0xdE54467873c3BCAA76421061036053e371721708   |
| Open Price Feed | USDC/USD   | 0xc629c26dced4277419cde234012f8160a0278a79   |
| _Uniswap v2_    | _USDC/ETH_ | _0xb4e16d0168e52d35cacd2c6185b44281ec28c9dc_ |
{% endtab %}

{% tab title="ETH/USD" %}
Поскольку не все оракулы имеют прямые пары с долларом США, протокол также извлекает цены для **ETH/USD**, чтобы рассчитать цены в долларах США с использованием ETH. Опять же, на всякий случай протокол выбирает наиболее выгодный для фонда, а не для отдельных персон.

| Оракул          | Пара    | Контракт                                   |
|:--------------- |:------- |:------------------------------------------ |
| Open Price Feed | ETH/USD | 0x922018674c12a7f0d394ebeef9b58f186cde13c1 |
| Chainlink       | ETH/USD | 0xF79D6aFBb6dA890132F9D7c355e3015f15F3406F |
{% endtab %}
{% endtabs %}

Возможно, что со временем в протокол будут добавлены дополнительные оракулы. Поддержка также может быть удалена, если какой-либо из этих оракулов станет ненадежным.

