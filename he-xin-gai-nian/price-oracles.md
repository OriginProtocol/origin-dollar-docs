# 价格神谕

OUSD旨在保持与 1 美元挂钩，并由基础稳定币 1：1支持。 这比听起来要棘手，因为这些基础稳定币一直在偏离它们想达到的 1 美元钉住汇率。 尽管大多数的每日波动不是很大，但过去曾发生过的重大的价格波动在将来很可能会再次发生。

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x5E01;</th>
      <th style="text-align:left"><b>&#x4F4E;</b>
      </th>
      <th style="text-align:left"><b>&#x9AD8;</b>
      </th>
      <th style="text-align:left"><b>Delta</b>
      </th>
      <th style="text-align:left"><b>&#x6765;&#x6E90;</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$ 0.929222</p>
        <p>2020&#x5E74;3&#x6708;13&#x65E5;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.11</p>
        <p>2018&#x5E74;10&#x6708;15&#x65E5;</p>
      </td>
      <td style="text-align:left">$ 0.180778</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$ 0.924188</p>
        <p>2020&#x5E74;8&#x6708;2&#x65E5;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.17</p>
        <p>2019&#x5E74;5&#x6708;08&#x65E5;</p>
      </td>
      <td style="text-align:left">$ 0.245812</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$ 0.945505</p>
        <p>2020&#x5E74;5&#x6708;10&#x65E5;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.11</p>
        <p>2020&#x5E74;3&#x6708;13&#x65E5;</p>
      </td>
      <td style="text-align:left">$ 0.164495</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$ 0.903243</p>
        <p>2019&#x5E74;11&#x6708;25&#x65E5;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.22</p>
        <p>2020&#x5E74;3&#x6708;13&#x65E5;</p>
      </td>
      <td style="text-align:left">$ 0.316757</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$ 0.849809</p>
        <p>2017&#x5E74;02&#x6708;02&#x65E5;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.21</p>
        <p>2017&#x5E74;5&#x6708;27&#x65E5;</p>
      </td>
      <td style="text-align:left">$ 0.360191</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$ 0.572521</p>
        <p>2015&#x5E74;3&#x6708;2&#x65E5;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.32</p>
        <p>2018&#x5E74;7&#x6708;24&#x65E5;</p>
      </td>
      <td style="text-align:left">$ 0.747479</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/tether/">CoinMarketCap</a>
      </td>
    </tr>
  </tbody>
</table>

为了在进入和退出时铸造和燃烧正确数量的 OUSD，智能合约需要准确定价进入和退出系统的 USDT，USDC 和 DAI。 它也需要一个可靠的方式来扩大供应以分配所赚取的利息，或者在基础资产价值发生负向变化时缩小供应。 作为去中心化协议，OUSD 必须依靠非中心化来源来获取这些价格。

{% hint style="info" %}
OUSD 从多个链上的预言服务器中获取价格，并使用对池最有利的汇率。
{% endhint %}

为了防止恶意攻击并鼓励长期投资者而非短期投机者，OUSD 合约比较多个来源的价格，并选择使用对整个资金池有利的汇率。 这种机制可以保护资金池中的资金免受套利者的侵害，并防止任何人能够利用因错误定价的预言而导致的任何暂时性的问题来耗尽共享资金池。

这保护池中的资金，同时奖励代币的长期持有者。 由于最安全的价格取决于交易的方向，因此 Origin oracle 公开了 `priceUSDMint()` 和 `priceUSDRedeem()`。 为了保持一致性，rebasing function使用 `priceUSDMint()` 。

这是 OUSD 正在使用的初始神谕：

{% embed url="https://compound.finance/docs/prices" caption="" %}

{% embed url="https://feeds.chain.link/eth-usd" caption="" %}

以下神谕已实施，但由于gas成本，目前未使用它们：

{% embed url="https://uniswap.org/docs/v2/core-concepts/oracles/" caption="" %}

{% tabs %}
{% tab title="DAI/USD" %}
以下神谕用于获取或计算 **DAI / USD** 的价格：

| 神谕（Oracle） | 对 | 合约 |
| :--- | :--- | :--- |
| 开放数据库 | DAI / USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| Chainlink | DAI / USD | 0xa7D38FBD325a6467894A13EeFD977aFE558bC1f0 |
| Chainlink | DAI/ETH | 0x037E8F2125bF532F3e228991e051c8A7253B642c |
| _Uniswap v2_ | _DAI/ETH_ | _0xA478c2975Ab1Ea89e8196811F51A7B7Ade33eB11_ |
{% endtab %}

{% tab title="USDT/USD" %}
以下神谕用于获取或计算 **USDT/USD** 的价格：

| O**racle** | 对 | 合约 |
| :--- | :--- | :--- |
| Chainlink | USDT / ETH | 0xa874fe207DF445ff19E7482C746C4D3fD0CB9AcE |
| 开放数据库 | USDC/USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| _Uniswap v2_ | _USDT/ETH_ | _0x0d4a11d5eeaac28ec3f61d100daf4d40471f1852_ |
{% endtab %}

{% tab title="USDC/USD" %}
以下神谕用于获取或计算 **USDC/USD** 的价格：

| O**racle** | 对 | 合约 |
| :--- | :--- | :--- |
| Chainlink | USDC/ETH | 0xdE54467873c3BCAA76421061036053e371721708 |
| 开放数据库 | USDC/USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| _Uniswap v2_ | _USDC / ETH_ | _0xb4e16d0168e52d35cacd2c6185b44281ec28c9dc_ |
{% endtab %}

{% tab title="ETH/USD" %}
由于不是所有神谕都有直接的美元对，因此该协议也获取 **ETH / USD** 的价格，以便使用 ETH 计算美元价格。 为了安全起见，协议会做出对于基金最有利益（而不是个人）的选择。

| 神谕（Oracle） | 对 | 合约 |
| :--- | :--- | :--- |
| 开放数据库 | ETH/USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| Chainlink | ETH/USD | 0xF79D6aFBb6dA890132F9D7c355e3015f15F3406F |
{% endtab %}
{% endtabs %}

接下来，其他的神谕也可能会被添加到协议中。 如果任何的一个神谕变得不可靠，我们也可能会取消对其神谕的支持。

