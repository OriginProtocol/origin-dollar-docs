# 가격 오라클

OUSD는 1 USD로 고정되고 기본 스테이블 코인과 1: 1로 지원되도록 설계되었습니다. 이러한 기본 스테이블 코인은 자신이 원하는 1 USD 페그에서 지속적으로 벗어나기 때문에 생각보다 까다롭습니다. 일일 변동의 대부분은 사소한 것이지만, 과거에 발생했던 주요 가격 변동이 있었다는 것을 보면 앞으로 다시 발생할 가능성을 배제할 수는 없습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xCF54;&#xC778;&#xC885;&#xB958;</th>
      <th style="text-align:left"><b>&#xB0AE;&#xC740;</b>
      </th>
      <th style="text-align:left"><b>&#xB192;&#xC740;</b>
      </th>
      <th style="text-align:left"><b>&#xB378;&#xD0C0;</b>
      </th>
      <th style="text-align:left"><b>&#xCD9C;&#xCC98;</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$ 0.929222</p>
        <p>2020 &#xB144; 3 &#xC6D4; 13 &#xC77C;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.11</p>
        <p>2018 &#xB144; 10 &#xC6D4; 15 &#xC77C;</p>
      </td>
      <td style="text-align:left">$ 0.180778</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$ 0.924188</p>
        <p>2020 &#xB144; 08 &#xC6D4; 02 &#xC77C;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.17</p>
        <p>2019 &#xB144; 05 &#xC6D4; 08 &#xC77C;</p>
      </td>
      <td style="text-align:left">$ 0.245812</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$0.945505</p>
        <p>2020 &#xB144; 05 &#xC6D4; 10 &#xC77C;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.11</p>
        <p>2020 &#xB144; 3 &#xC6D4; 13 &#xC77C;</p>
      </td>
      <td style="text-align:left">$ 0.164495</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$ 0.903243</p>
        <p>2019 &#xB144; 11 &#xC6D4; 25 &#xC77C;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.22</p>
        <p>2020 &#xB144; 3 &#xC6D4; 13 &#xC77C;</p>
      </td>
      <td style="text-align:left">$ 0.316757</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$ 0.849809</p>
        <p>2017 &#xB144; 2 &#xC6D4; 02 &#xC77C;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.21</p>
        <p>2017 &#xB144; 05 &#xC6D4; 27 &#xC77C;</p>
      </td>
      <td style="text-align:left">$ 0.360191</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$ 0.572521</p>
        <p>2015 &#xB144; 3 &#xC6D4; 02 &#xC77C;</p>
      </td>
      <td style="text-align:left">
        <p>$ 1.32</p>
        <p>2018 &#xB144; 7 &#xC6D4; 24 &#xC77C;</p>
      </td>
      <td style="text-align:left">$ 0.747479</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/tether/">CoinMarketCap</a>
      </td>
    </tr>
  </tbody>
</table>

출입시 적절한 수의 OUSD를 발행하고 소각하기 위해 스마트 컨트렉트는 시스템에 들어오고 나가는 USDT, USDC 및 DAI의 가격을 정확하게 책정해야합니다. 또한 획득한 이자를 분배하기 위해 공급을 확장하거나 기초 자산의 가치에 부정적인 변화가 있을 경우 공급을 계약하는 신뢰할 수있는 방법이 필요합니다. 탈 중앙화된 프로토콜로서 OUSD는 이러한 가격에 대해 비 중앙화 소스에 의존해야합니다.

{% hint style="info" %}
OUSD는 여러 온 체인 오라클에서 가격을 가져와 풀에 가장 유리한 환율을 사용합니다.
{% endhint %}

악의적인 공격을 방지하고 단기 투기자들로 하여금 장기 투자자가 될 것을 장려하기 위해, OUSD 컨트렉트는 여러 소스의 가격 피드를 비교하고 개인에 비해 전체 풀에 이익이되는 환율을 사용합니다. 해당 메커니즘은 중재자로부터 풀의 자금을 보호하고 개인이 공유 자산 풀을 고갈시키기 위해 가격이 잘못 책정 된 오라클로 인한 일시적인 비 효율성을 이용할 수 없도록합니다.

이는 장기 보유자에게 보상을 제공하면서 풀의 자금을 보호할 수 있습니다. 가장 안전한 가격은 거래 방향에 따라 다르기 때문에 오리진 오라클은 `priceUSDMint ()` 과 `priceUSDRedeem ()`모두 노출합니다. Rebasing 함수는 일관성을 위해 `priceUSDMint ()` 을 사용합니다.

다음은 OUSD에서 사용중인 초기 오라클 세트입니다.

{% embed url="https://compound.finance/docs/prices" caption="" %}

{% embed url="https://feeds.chain.link/eth-usd" caption="" %}

다음 오라클들도 구현되었지만, 가스 비용으로 인해 현재는 사용되고 있지 않습니다.

{% embed url="https://uniswap.org/docs/v2/core-concepts/oracles" caption="" %}

{% tabs %}
{% tab title="Core" %}
다음 오라클은 **DAI / USD의 가격을 가져 오거나 계산하는 데 사용됩니다.**

| 오라클 | 쌍\(pair\) | 컨트렉트 |
| :--- | :--- | :--- |
| 오픈 가격 피드 | DAI / USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| 체인 링크 | DAI / USD | 0xa7D38FBD325a6467894A13EeFD977aFE558bC1f0 |
| 체인 링크 | DAI / ETH | 0x037E8F2125bF532F3e228991e051c8A7253B642c |
| _유니스왑\(Uniswap\) v2_ | _DAI / ETH_ | _0xA478c2975Ab1Ea89e8196811F51A7B7Ade33eB11_ |
{% endtab %}

{% tab title="Core" %}
다음 오라클은 **DAI / USD의 가격을 가져오거나 계산하는데 사용됩니다.**

| &lt;/strong&gt;오라클&lt;/0&gt; | 쌍\(pair\) | 컨트렉트 |
| :--- | :--- | :--- |
| 체인 링크 | USDT / ETH | 0xa874fe207DF445ff19E7482C746C4D3fD0CB9AcE |
| 오픈 가격 피드 | USDC / USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| _유니스왑\(Uniswap\) v2_ | _USDT / ETH_ | _0x0d4a11d5eeaac28ec3f61d100daf4d40471f1852_ |
{% endtab %}

{% tab title="Core" %}
다음 오라클은 **DAI / USD의 가격을 가져오거나 계산하는데 사용됩니다.**

| &lt;/strong&gt;오라클&lt;/0&gt; | 쌍\(pair\) | 컨트렉트 |
| :--- | :--- | :--- |
| 체인 링크 | USDT / ETH | 0xdE54467873c3BCAA76421061036053e371721708 |
| 오픈 가격 피드 | USDC / USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| _유니스왑\(Uniswap\) v2_ | _USDT / ETH_ | _0xb4e16d0168e52d35cacd2c6185b44281ec28c9dc_ |
{% endtab %}

{% tab title="Core" %}
모든 오라클에 직접 USD 쌍이있는 것은 아니므로 프로토콜은 ETH를 사용하여 USD 가격을 계산하기 위해 **ETH / USD** 의 가격도 가져옵니다. 다시 말하지만, 안전을 위해 프로토콜은 개인 대신 펀드에 가장 유리한 것을 선택합니다.

| 오라클 | 쌍\(pair\) | 컨트렉트 |
| :--- | :--- | :--- |
| 오픈 가격 피드 | ETH / USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| 체인 링크 | ETH / USD | 0xF79D6aFBb6dA890132F9D7c355e3015f15F3406F |
{% endtab %}
{% endtabs %}

시간이 지남에 따라 추가 스테이블 코인이 프로토콜에 추가 될 수 있습니다. 이러한 오라클 중 하나라도 신뢰할 수 없는 경우 지원이 제거 될 수도 있습니다.

