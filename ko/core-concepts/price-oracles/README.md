# 가격 오라클(Price Oracles)

OUSD는 1 USD로 고정되고 기본 스테이블 코인과 1: 1로 지원되도록 설계되었습니다. 이러한 기본 스테이블 코인은 자신이 원하는 1 USD 페그에서 지속적으로 벗어나기 때문에 생각보다 까다롭습니다. 일일 변동의 대부분은 사소한 것이지만, 과거에 발생했던 주요 가격 변동이 있었다는 것을 보면 앞으로 다시 발생할 가능성을 배제할 수는 없습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">코인종류</th>
      <th style="text-align:left"><b>낮은</b>
      </th>
      <th style="text-align:left"><b>높은</b>
      </th>
      <th style="text-align:left"><b>델타</b>
      </th>
      <th style="text-align:left"><b>출처</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$ 0.929222</p>
        <p>2020 년 3 월 13 일</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.11</p>
        <p>2018 년 10 월 15 일</p>
      </td>
      <td style="text-align:left">$ 0.180778</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$ 0.924188</p>
        <p>2020 년 08 월 02 일</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.17</p>
        <p>2019 년 05 월 08 일</p>
      </td>
      <td style="text-align:left">$ 0.245812</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$0.945505</p>
        <p>2020 년 05 월 10 일</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.11</p>
        <p>2020 년 3 월 13 일</p>
      </td>
      <td style="text-align:left">$ 0.164495</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$ 0.903243</p>
        <p>2019 년 11 월 25 일</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.22</p>
        <p>2020 년 3 월 13 일</p>
      </td>
      <td style="text-align:left">$ 0.316757</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$ 0.849809</p>
        <p>2017 년 2 월 02 일</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.21</p>
        <p>2017 년 05 월 27 일</p>
      </td>
      <td style="text-align:left">$ 0.360191</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$ 0.572521</p>
        <p>2015 년 3 월 02 일</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.32</p>
        <p>2018 년 7 월 24 일</p>
      </td>
      <td style="text-align:left">$ 0.747479</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/tether/">CoinMarketCap</a>
      </td>
    </tr>
  </tbody>
</table>

리베이스 기능은 단순성을 위해 1개의 스테이블 코인을 1개의 OUSD로 취급하고 기본 스테이블 코인 가격의 일일 변동에 의해 영향을 받는 OUSD 잔액을 보호합니다. Since the rebase function only counts coins, OUSD balances should only increase.

In order to mint and redeem the appropriate number of OUSD on entry and exit, the smart contracts need to accurately price the USDT, USDC, and DAI that is entering and exiting the system. As a decentralized protocol, OUSD must rely on non-centralized sources for these prices.

{% hint style="info" %}
OUSD fetches the price from multiple on-chain oracles and uses the exchange rate that is most advantageous for the vault when minting or redeeming.
{% endhint %}

In order to prevent malicious attacks and to encourage long-term investors over short-term speculators, the OUSD contract compares price feeds from multiple sources and will use whichever exchange rate benefits the entire vault over the individual. This mechanism protects the vault funds from arbitrageurs and prevents any individual from being able to take advantage of any temporary inefficiencies caused by mispriced oracles to deplete the shared pool of assets.

This protects the funds in the vault while rewarding long-term holders. Since the safest price depends on the direction of the trade, the Origin oracle exposes both a `priceUSDMint()` and a `priceUSDRedeem()`.

OUSD uses Chainlink as oracle for DAI, USDC and USDT.

{% embed url="https://feeds.chain.link/eth-usd" caption="" %}

The specific smart contract address for each oracle being used are listed on our [registry](../../smart-contracts/registry.md) page.

It is possible that additional oracles will be added to the protocol over time. Support may also be removed if any of these oracles become unreliable.

