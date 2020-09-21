# 작동 방법

## 100 % 지원 및 안정

Origin Dollar \(OUSD\) is an ERC-20 compliant token for the Ethereum network.

OUSD is a stable currency that is backed 1:1 by other stablecoins like USDT, USDC and DAI. 결과적으로 1 OUSD는 항상 1 USD 가치에 매우 가깝습니다.

{% hint style="success" %}
1 OUSD = 1 USD
{% endhint %}

## OUSD 민팅\(Minting\)

사용자는 공식 [Origin Dollar DApp](https://github.com/oplabs/origin-dollar-docs/tree/fcbb45ee8da4bb026f7706157523003e0a849df4/www.ousd.com)에서 기존 스테이블코인  \(현재 USDT, USDC, DAI \) 을 OUSD로 전환합니다. 발행된 OUSD는 즉시 복리로 수익을 발생시키기 시작합니다.

**OUSD 사용하기**

Users can convert their OUSD back into other stablecoins at any time using the [Origin Dollar DApp](https://github.com/oplabs/origin-dollar-docs/tree/fcbb45ee8da4bb026f7706157523003e0a849df4/www.ousd.com). A 0.5% exit fee is charged upon redemption and is distributed as additional yield to the remaining participants in the pool. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from syphoning stablecoins from the pool in the event of mispricings of of the underlying assets. The fee exists to incentivize long-term holders over short-term speculators.

Upon redemption, the smart contract will determine which stablecoin\(s\) to return to the user. In the current implementation, the pool will return coins in the same ratio as the current holdings. This lack of user optionality also protects the pool as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}
There is a **0.5% exit fee** and the user doesn't get to pick which stablecoins they receive.
{% endhint %}

## **수확량 농업\(Automated Yield Farming\)**

OUSD generates yields by deploying the underlying stablecoins that were deposited to the OUSD smart contract to other DeFi protocols such as Compound, Aave, Uniswap, Balancer, and Curve. It is expected there will be new diversified strategies added to the pool every month. Collected interest, trading fees, and rewards tokens are pooled and converted to stablecoins to produce OUSD-denominated yields. Over time, the protocol will move assets in and out of different liquidity pools in order to provide the best yield to the holders of OUSD.

## **공급 탄력성**

생성된 수익은 통화 공급의 지속적인 리베이스\(rebase\) 를 통해 OUSD 보유자에게 전달됩니다. OUSD는 프로토콜이 생성한 수익률에 따라 통화 공급을 지속적으로 조정합니다. 이를 통해 OUSD의 가격은 1달러로 고정되는 반면 토큰 보유자의 지갑 잔액은 프로토콜로 얻은 수익률을 반영하기 위해 실시간으로 조정됩니다.

최종 결과는 사용하기 쉽고 자동으로 큰 수익을 얻으며 기존 스테이블코인 보다 더 보유하는 것이 바람직한 스테이블코인 입니다.

