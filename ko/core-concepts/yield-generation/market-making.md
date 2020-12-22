# 마켓메이킹

**탈 중앙화 거래소에서 지분 소유**

자동화 된 마켓 메이커 \ (AMMs \) 는 이더리움 네트워크에서 선호하는 탈 중앙화 거래소 형태로 빠르게 부상했습니다. 이는 중앙 집중식 거래소에서의 순간 및 저소량 경험에 필적할 수 있는 이더리움 1.0의 주문서 DEX의 지원이 어렵기 때문이기도 합니다. 또한 유니스왑(Uniswap) 과 같은 AMM은 상대적으로 사용자 친화적이고 가스효율적입니다.

AMM은 유동성 공급자가 유동성을 공급할 때만 새로운 시장을 활성화 할 수 있습니다. 유동성을 제공하는 대가로 유동성 공급자는 다른 사용자가 토큰을 교환 할 때 거래 수수료를받습니다. 예를 들어 트레이더가 유니스왑(Uniswap) 에서 USDT를 USDC로 교환 할 때 현재 가스 수수료 외에 0.3 %가 부과됩니다. 이 수수료는 USDT-USDC 쌍의 유동성 공급자가 제공 한 총 유동성 비율에 따라 비례 배분됩니다.

{% hint style="info" %}
[무상 손실](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) 은 이해해야 할 중요한 위험 요소이지만이 문제는 OUSD가 거의 동일한 가치의 스테이블 코인에 유동성을 제공함으로써 대부분 완화됩니다.
{% endhint %}

OUSD 프로토콜은 USDT, USDC 및 DAI를 거래량 및 보상 토큰에 의해 결정된 고성능 유동성 풀로 라우팅합니다 \ (예: 밸런서(Balancer)는 BAL 토큰을 유동성 공급자에게 보상합니다 \). 수익은 OUSD 보유자에게 전달됩니다.

We are currently integrated with the following automated market maker:

{% page-ref page="../supported-strategies/curve.md" %}

We are intending to integrate with the following automated market makers:

{% page-ref page="../supported-strategies/uniswap.md" %}

{% page-ref page="../supported-strategies/balancer.md" %}





