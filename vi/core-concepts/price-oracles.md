# Ước tính giá

OUSD được thiết kế để duy trì ở mức 1 USD và được hỗ trợ 1:1 bằng các stablecoin. Trên thực tế, việc duy trì tỉ lệ này phức tạp hơn nhiều vì giá của các stablecoin thường sẽ chênh lệch so với mức 1$. Thường thì những biến động trên khá nhỏ, tuy nhiên, không ngoại trừ trường hợp có thể có biến động lớn xảy ra như đã từng gặp trong quá khứ.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Coin</th>
      <th style="text-align:left"><b>Thấp</b>
      </th>
      <th style="text-align:left"><b>Cao</b>
      </th>
      <th style="text-align:left"><b>Chênh lệch</b>
      </th>
      <th style="text-align:left"><b>Nguồn</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>0,929222$</p>
        <p>13/03/2020</p>
      </td>
      <td style="text-align:left">
        <p>1,11$</p>
        <p>15/10/2018</p>
      </td>
      <td style="text-align:left">0,180778$</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>0,924188$</p>
        <p>02/08/2020</p>
      </td>
      <td style="text-align:left">
        <p>1,17$</p>
        <p>08/05/2019</p>
      </td>
      <td style="text-align:left">0,245812$</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>0,945505$</p>
        <p>10/05/2020</p>
      </td>
      <td style="text-align:left">
        <p>1,11$</p>
        <p>13/03/2020</p>
      </td>
      <td style="text-align:left">0,164495$</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>0,903243$</p>
        <p>25/11/2019</p>
      </td>
      <td style="text-align:left">
        <p>1,22$</p>
        <p>13/03/2020</p>
      </td>
      <td style="text-align:left">0,316757$</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>0,849809$</p>
        <p>02/02/2017</p>
      </td>
      <td style="text-align:left">
        <p>1,21$</p>
        <p>27/05/2017</p>
      </td>
      <td style="text-align:left">0,360191$</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>0,572521$</p>
        <p>02/03/2015</p>
      </td>
      <td style="text-align:left">
        <p>1,32$</p>
        <p>24/07/2018</p>
      </td>
      <td style="text-align:left">0,747479$</td>
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

