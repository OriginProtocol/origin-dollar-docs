# Price Oracles

OUSD is designed to stay pegged at 1 USD and be 1:1 backed with its underlying stablecoins. However, it's important to note that these other stablecoins are constantly deviating from their own desired 1 USD pegs. While the majority of daily fluctuations are minor, there have been major swings in price that have occurred in the past and are likely to occur again in the future.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Coin</th>
      <th style="text-align:left"><b>Source</b>
      </th>
      <th style="text-align:left"><b>Low</b>
      </th>
      <th style="text-align:left"><b>High</b>
      </th>
      <th style="text-align:left"><b>Delta</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap</a>
      </td>
      <td style="text-align:left">
        <p>$0.929222</p>
        <p>Mar 13, 2020</p>
      </td>
      <td style="text-align:left">
        <p>$1.11</p>
        <p>Oct 15, 2018</p>
      </td>
      <td style="text-align:left">$0.180778</td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
      <td style="text-align:left">
        <p>$0.924188</p>
        <p>Aug 02, 2020</p>
      </td>
      <td style="text-align:left">
        <p>$1.17</p>
        <p>May 08, 2019</p>
      </td>
      <td style="text-align:left">$0.245812</td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap</a>
      </td>
      <td style="text-align:left">
        <p>$0.945505</p>
        <p>May 10, 2020</p>
      </td>
      <td style="text-align:left">
        <p>$1.11</p>
        <p>Mar 13, 2020</p>
      </td>
      <td style="text-align:left">$0.164495</td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
      <td style="text-align:left">
        <p>$0.903243</p>
        <p>Nov 25, 2019</p>
      </td>
      <td style="text-align:left">
        <p>$1.22</p>
        <p>Mar 13, 2020</p>
      </td>
      <td style="text-align:left">$0.316757</td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/tether/">CoinMarketCap</a>
      </td>
      <td style="text-align:left">
        <p>$0.849809</p>
        <p>Feb 02, 2017</p>
      </td>
      <td style="text-align:left">
        <p>$1.21</p>
        <p>May 27, 2017</p>
      </td>
      <td style="text-align:left">$0.360191</td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
      <td style="text-align:left">
        <p>$0.572521</p>
        <p>Mar 02, 2015</p>
      </td>
      <td style="text-align:left">
        <p>$1.32</p>
        <p>Jul 24, 2018</p>
      </td>
      <td style="text-align:left">$0.747479</td>
    </tr>
  </tbody>
</table>

In order to mint and burn the appropriate number of OUSD on entry and exit, the smart contracts need to accurately price the USDT, USDC, and DAI that is entering and exiting the system. It also needs a reliable way of expanding the supply to distribute the interest that is earned, or contracting supply if there is a negative change in the value of the underlying assets. As a decentralized protocol, OUSD must rely on non-centralized sources for these prices.

In order to prevent malicious attacks and to encourage long-term investors over short-term speculators, the OUSD contract compares price feeds from multiple sources and will use whichever exchange rate benefits the entire pool over the individual. This mechanism protects the pool's funds from arbitrageurs and prevents any individual from being able to take advantage of any temporary inefficiencies caused by mispriced oracles to deplete the shared pool of assets. 



