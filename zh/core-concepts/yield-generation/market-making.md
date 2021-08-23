# 做市

**持有去中心化交易所中的股份**

自动化做市商\(AMMs\) 迅速崛起，成为以太坊网络上去中心化交易的首选形式。 部分原因是由于在以太坊1.0上支持可以与中心化交易所的速度和滑点体验的订单簿 DEX 的困难。 此外，诸如 Uniswap 的 AMM 相对用户友好且gas费用较低。

仅当流动性提供者提供流动性 (例如，为某交易对或资金池提供多个代币）时，AMMs 才能启动新市场。 作为提供流动性的回报，当其他用户交换代币时，流动性提供者将获得交易费奖励。 例如，在 Uniswap 上将 USDT 换成 USDC 时，目前需支付gas费，还要额付0.3％ 的交易手续费。 这些费用根据其提供的总流动性百分比按比例分配给 USDT-USDC 对的流动性提供者。

{% hint style="info" %}
[永久损失](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) 是需要理解的重要风险因素。但是由于 OUSD 只为近似相等价值的稳定币提供流动性，因此从而大大缓解了这种担忧。
{% endhint %}

OUSD 协议将 USDT，USDC 和 DAI 路由到根据交易量和奖励代币而决定的高性能流动性池， (例如 Balancer 将 BAL 代币奖励给流动性提供商)。 然后，收益将分发给OUSD持有者。

We are currently integrated with the following automated market maker:

{% page-ref page="../supported-strategies/curve.md" %}

We are intending to integrate with the following automated market makers:





