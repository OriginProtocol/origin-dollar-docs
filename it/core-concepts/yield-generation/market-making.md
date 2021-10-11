# Market Making

**Custodisci il tuo stake negli Exchanges Decentralizzati**

Automated market makers (AMMs) have quickly risen as the preferred form of decentralized exchange on the Ethereum network. Ciò in parte è dovuto alla difficoltà di supportare gli order book DEX su Ethereum 1.0 che possano competere con gli attuali exchange centralizzati, istantanei e a basso slippage. Inoltre, gli AMM come Uniswap sono relativamente user-friendly ed efficienti dal punto di vista del gas.

AMMs can only enable new markets when liquidity providers supply liquidity (e.g. multiple tokens for given trading pairs or pools). In cambio per fornire liquidità, i liquidity providers sono ricompensati con le commissioni di trading quando altri utenti swappano i token. For example, when traders swap two tokens on Uniswap v3, they are currently charged anywhere between 0.05% and 1% on top of the gas fees. These fees are distributed pro-rata to liquidity providers of the pair based on the percentage of total liquidity that they have provided.

{% hint style="info" %}
[Impermanent loss](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) è un fattore di rischio importante da capire, ma questa preoccupazione è altamente mitigata dal fatto che OUSD fornisce liquidità solo per stablecoin che hanno approssimatamente egual valore.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens (e.g. Curve rewards CRV tokens to liquidity providers). Gli Yields vengono quindi trasferiti ai detentori di OUSD.

We are currently integrated with the following automated market maker:

{% content-ref url="../supported-strategies/curve.md" %}
[curve.md](../supported-strategies/curve.md)
{% endcontent-ref %}



