# Market Making

**Own your Stake in Decentralized Exchanges**

Automated market makers \(AMMs\) have quickly risen as the preferred form of decentralized exchange on the Ethereum network. This is in part due to the difficulty of supporting order book DEXes on Ethereum 1.0 that can rival the instant and low-slippage experiences on centralized exchanges. Further, AMMs like Uniswap are relatively user-friendly and gas-efficient to use.

AMMs can only enable new markets when liquidity providers supply liquidity \(e.g. multiple tokens for given trading pairs or pools\). In return for providing liquidity, liquidity providers are rewarded with trading fees when other users swap tokens. For example, when traders swap USDT for USDC on Uniswap, they are currently charged 0.3% on top of gas fees. These fees are distributed pro-rata to liquidity providers on the USDT-USDC pair based on the percentage of total liquidity that they have provided. 

{% hint style="info" %}
[Impermanent loss](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) is an important risk factor to understand, but this concern is largely mitigated by OUSD only providing liquidity for stablecoins of approximately equal value.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens \(e.g. Balancer rewards BAL tokens to liquidity providers\). Yields are then passed on to OUSD holders.

We are currently integrated with the following automated market maker:

{% page-ref page="../supported-strategies/curve.md" %}

We are intending to integrate with the following automated market makers:

{% page-ref page="../supported-strategies/uniswap.md" %}

{% page-ref page="../supported-strategies/balancer.md" %}





