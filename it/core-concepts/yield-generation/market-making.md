# Market Making

**Custodisci il tuo stake negli Exchanges Decentralizzati**

I market maker automatizzati \(AMMs\) sono cresciuti rapidamente come forma preferita di scambio decentralizzato sul network di Ethereum. Ciò in parte è dovuto alla difficoltà di supportare gli order book DEX su Ethereum 1.0 che possano competere con gli attuali exchange centralizzati, istantanei e a basso slippage. Inoltre, gli AMM come Uniswap sono relativamente user-friendly ed efficienti dal punto di vista del gas.

AMMs can only enable new markets when liquidity providers supply liquidity \(e.g. multiple tokens for given trading pairs or pools\). In return for providing liquidity, liquidity providers are rewarded with trading fees when other users swap tokens. For example, when traders swap USDT for USDC on Uniswap, they are currently charged 0.3% on top of gas fees. These fees are distributed pro-rata to liquidity providers on the USDT-USDC pair based on the percentage of total liquidity that they have provided.

{% hint style="info" %}
[Impermanent loss](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) is an important risk factor to understand, but this concern is largely mitigated by OUSD only providing liquidity for stablecoins of approximately equal value.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens \(e.g. Balancer rewards BAL tokens to liquidity providers\). Yields are then passed on to OUSD holders.

We intend to integrate directly with at least the following automated market makers:

{% page-ref page="../supported-strategies/uniswap.md" %}

{% page-ref page="../supported-strategies/curve.md" %}

{% page-ref page="../supported-strategies/balancer.md" %}





