# Collectivist Pricing

{% hint style="info" %}
OUSD fetches the price from multiple on-chain oracles and uses the exchange rate that is most advantageous for the group and the least beneficial for the individual.
{% endhint %}

Having trustworthy pricing data is vital to the security of the entire system. To minimize the risk of a single oracle being manipulated or compromised, OUSD relies on multiple different on-chain pricing feeds to determine a fair exchange rate between OUSD and other stable coins. If the reported prices differ, the smart contract will use the exchange rate that is most advantageous for the group and the least beneficial for the individual. This protects the funds in the pool while rewarding long-term holders. Since the safest price depends on the direction of the trade, the Origin oracle exposes both a `mintPrice()` and a `redeemPrice()`. The rebasing function utilizes the `mintPrice()` for consistency.

Here is the initial set of oracles that are being used by OUSD: 

{% embed url="https://compound.finance/docs/prices" %}

{% embed url="https://feeds.chain.link/eth-usd" %}

{% embed url="https://makerdao.com/en/feeds/" %}

{% embed url="https://uniswap.org/docs/v2/core-concepts/oracles/" %}



