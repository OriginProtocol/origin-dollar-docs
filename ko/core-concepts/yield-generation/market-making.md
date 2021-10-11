# 마켓메이킹

**탈 중앙화 거래소에서 지분 소유**

Automated market makers (AMMs) have quickly risen as the preferred form of decentralized exchange on the Ethereum network. 이는 중앙 집중식 거래소에서의 순간 및 저소량 경험에 필적할 수 있는 이더리움 1.0의 주문서 DEX의 지원이 어렵기 때문이기도 합니다. 또한 유니스왑(Uniswap) 과 같은 AMM은 상대적으로 사용자 친화적이고 가스효율적입니다.

AMMs can only enable new markets when liquidity providers supply liquidity (e.g. multiple tokens for given trading pairs or pools). 유동성을 제공하는 대가로 유동성 공급자는 다른 사용자가 토큰을 교환 할 때 거래 수수료를받습니다. For example, when traders swap two tokens on Uniswap v3, they are currently charged anywhere between 0.05% and 1% on top of the gas fees. These fees are distributed pro-rata to liquidity providers of the pair based on the percentage of total liquidity that they have provided.

{% hint style="info" %}
[무상 손실](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) 은 이해해야 할 중요한 위험 요소이지만이 문제는 OUSD가 거의 동일한 가치의 스테이블 코인에 유동성을 제공함으로써 대부분 완화됩니다.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens (e.g. Curve rewards CRV tokens to liquidity providers). 수익은 OUSD 보유자에게 전달됩니다.

We are currently integrated with the following automated market maker:

{% content-ref url="../supported-strategies/curve.md" %}
[curve.md](../supported-strategies/curve.md)
{% endcontent-ref %}



