# Pazar yapımı

**Merkezi Olmayan Borsalarda Payınızı Sahibi Olun**

Automated market makers (AMMs) have quickly risen as the preferred form of decentralized exchange on the Ethereum network. Bu kısmen, merkezi borsalardaki anlık ve düşük kayma deneyimlerine rakip olabilecek Ethereum 1.0'daki sipariş defteri DEX'leri desteklemenin zorluğundan kaynaklanıyor. Ayrıca, Uniswap gibi AMM'ler nispeten kullanıcı dostudur ve kullanımları gaz verimlidir.

AMMs can only enable new markets when liquidity providers supply liquidity (e.g. multiple tokens for given trading pairs or pools). Likidite sağlama karşılığında likidite sağlayıcıları, diğer kullanıcılar token takas ettiğinde alım satım ücretleri ile ödüllendirilir. For example, when traders swap two tokens on Uniswap v3, they are currently charged anywhere between 0.05% and 1% on top of the gas fees. These fees are distributed pro-rata to liquidity providers of the pair based on the percentage of total liquidity that they have provided.

{% hint style="bilgi" %}
[Kalıcı olmayan kayıp](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) , anlaşılması gereken önemli bir risk faktörüdür, ancak bu endişe, yalnızca OUSD tarafından yaklaşık olarak eşit değerdeki stabilcoinler için likidite sağlayarak büyük ölçüde hafifletilir.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens (e.g. Curve rewards CRV tokens to liquidity providers). Daha sonra getiriler OUSD sahiplerine aktarılır.

We are currently integrated with the following automated market maker:

{% content-ref url="../supported-strategies/curve.md" %}
[curve.md](../supported-strategies/curve.md)
{% endcontent-ref %}



