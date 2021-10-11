# 做市

**持有去中心化交易所中的股份**

Automated market makers (AMMs) have quickly risen as the preferred form of decentralized exchange on the Ethereum network. 部分原因是由于在以太坊1.0上支持可以与中心化交易所的速度和滑点体验的订单簿 DEX 的困难。 此外，诸如 Uniswap 的 AMM 相对用户友好且gas费用较低。

AMMs can only enable new markets when liquidity providers supply liquidity (e.g. multiple tokens for given trading pairs or pools). 作为提供流动性的回报，当其他用户交换代币时，流动性提供者将获得交易费奖励。 For example, when traders swap two tokens on Uniswap v3, they are currently charged anywhere between 0.05% and 1% on top of the gas fees. These fees are distributed pro-rata to liquidity providers of the pair based on the percentage of total liquidity that they have provided.

{% hint style="info" %}
[永久损失](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) 是需要理解的重要风险因素。但是由于 OUSD 只为近似相等价值的稳定币提供流动性，因此从而大大缓解了这种担忧。
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens (e.g. Curve rewards CRV tokens to liquidity providers). 然后，收益将分发给OUSD持有者。

We are currently integrated with the following automated market maker:

{% content-ref url="../supported-strategies/curve.md" %}
[curve.md](../supported-strategies/curve.md)
{% endcontent-ref %}



