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

Функция перераспределения обрабатывает 1 стейблкоин как 1 OUSD для простоты и для защиты баланса OUSD от ежедневных колебаний цены базовых стейблкоинов. Поскольку функция перераспределения считает только монеты, баланс OUSD должен только увеличиваться.

Чтобы создать и высвободить соответствующее количество OUSD при входе и выходе, смарт-контракты должны точно определять цену на USDT, USDC и DAI, которые входят в систему и выходят из нее. Как децентрализованный протокол, OUSD должен полагаться на не являющимися централизованными источники этих цен.

{% hint style="info" %}
OUSD получает цену от нескольких оракулов в сети и использует обменный курс, который является наиболее выгодным для хранилища, когда происходит процесс создания новых монет или их высвобождение.
{% endhint %}

Чтобы предотвратить злонамеренные атаки и больше поощрять долгосрочных инвесторов, чем краткосрочных спекулянтов, контракт OUSD сравнивает потоки цен из нескольких источников и использует тот обменный курс, который выгоден для всего хранилища, а не для отдельных лиц. Этот механизм защищает средства, находящиеся в хранилище, от арбитражеров и никому не позволяет воспользоваться любой временной неэффективностью, вызванной ошибкой оракулов, для истощения общего пула активов.

Это защищает средства в хранилище и поощряет долгосрочных держателей. Поскольку самая безопасная цена зависит от направления сделки, оракул Origin предоставляет как `priceUSDMint()`, так и `priceUSDRedeem()`.

OUSD uses Chainlink as oracle for DAI, USDC and USDT.

{% embed url="https://feeds.chain.link/eth-usd" caption="" %}

The specific smart contract address for each oracle being used are listed on our [registry](../../smart-contracts/registry.md) page.

It is possible that additional oracles will be added to the protocol over time. Support may also be removed if any of these oracles become unreliable.

