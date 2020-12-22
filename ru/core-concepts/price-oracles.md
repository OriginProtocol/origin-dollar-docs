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

The rebasing function treats 1 stablecoin as 1 OUSD for simplicity and to protect OUSD balances from being affected by the daily fluctuations in the price of the underlying stablecoins. Since the rebase function only counts coins, OUSD balances should only increase.

In order to mint and redeem the appropriate number of OUSD on entry and exit, the smart contracts need to accurately price the USDT, USDC, and DAI that is entering and exiting the system. As a decentralized protocol, OUSD must rely on non-centralized sources for these prices.

{% hint style="info" %}
OUSD fetches the price from multiple on-chain oracles and uses the exchange rate that is most advantageous for the vault when minting or redeeming.
{% endhint %}

In order to prevent malicious attacks and to encourage long-term investors over short-term speculators, the OUSD contract compares price feeds from multiple sources and will use whichever exchange rate benefits the entire vault over the individual. This mechanism protects the vault funds from arbitrageurs and prevents any individual from being able to take advantage of any temporary inefficiencies caused by mispriced oracles to deplete the shared pool of assets.

This protects the funds in the vault while rewarding long-term holders. Since the safest price depends on the direction of the trade, the Origin oracle exposes both a `priceUSDMint()` and a `priceUSDRedeem()`.

Here is the initial set of oracles that are being used by OUSD:

{% embed url="https://compound.finance/docs/prices" caption="" %}

{% embed url="https://feeds.chain.link/eth-usd" caption="" %}

The following oracles have been implemented, but are not currently being used due to gas costs:

{% embed url="https://uniswap.org/docs/v2/core-concepts/oracles/" caption="" %}

The specific smart contract address for each oracle being used are listed on our [registry](../smart-contracts/registry.md) page.

It is possible that additional oracles will be added to the protocol over time. Support may also be removed if any of these oracles become unreliable.

