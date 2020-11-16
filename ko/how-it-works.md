# 작동 방법

#### 100 % 지원 및 안정

오리진 달러 \ (OUSD \) 는 이더리움 네트워크를 위한 비표준 ERC-20 토큰입니다.

OUSD는 USDT, USDC 및 DAI와 같은 검증된 스테이블 코인이 1:1로 지원되는 안정적인 통화입니다. 결과적으로, 1 OUSD는 항상 1 USD와 비슷한 가치를 가지게 됩니다.

{% hint style="success" %}
1 OUSD = 1 USD
{% endhint %}

#### OUSD 발행(Minting)

사용자는 공식 [오리진 달러 디앱(DApp)](www.ousd.com)에서 기존 스테이블 코인 \ (현재 USDT, USDC, DAI \) 을 OUSD로 전환합니다. 발행된 OUSD는 즉시 복리로 수익을 발생시키기 시작합니다.

**OUSD 사용하기**

사용자는 [오리진 달러 디앱(DApp)](www.ousd.com)을 사용하여 언제든지 OUSD를 다른 스테이블 코인(stablecoin) 으로 전환 할 수 있습니다. A 0.5% exit fee is charged upon redemption and is distributed as additional yield to the remaining participants in the vault. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from syphoning stablecoins from the vault in the event of mispricings of of the underlying assets. 해당 수수료는 단기 투기자 보다는 장기 보유자가 될 것을 장려하기 위해 존재합니다.

상환시 스마트 컨트렉트는 사용자에게 반환할 스테이블 코인을 결정합니다. In the current implementation, the vault will return coins in the same ratio as the current holdings. This lack of user optionality also protects the vault as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}
**0.5 % 출금 수수료** 가 있으며, 사용자는 어떤 종류의 스테이블 코인을 받을지를 직접 선택할 수는 없습니다.
{% endhint %}

#### **자동화 이자 농사(Automated Yield Farming)**

OUSD는 OUSD 스마트 컨트렉트에 예치된 기본 스테이블 코인을 컴파운드(Compound), 에이브(Aave), 유니스왑(Uniswap), 밸런서(Balance) 및 커브(Curve) 와 같은 다른 디파이(DeFi) 프로토콜에 배포하여 수익을 창출합니다. It is expected there will be new diversified strategies added to the vault every month. 수집된 이자, 거래 수수료 및 보상 토큰은 OUSD 표시 수익률을 생성하기 위해 풀링(pooling) 되고 청산됩니다. 시간이 지남에 따라 프로토콜은 OUSD 보유자에게 최상의 수익을 제공하기 위해 프로그래밍 방식으로 자산을 다른 유동성 풀(liquidity pool) 안팎으로 이동합니다.

#### **공급 탄력성**

생성된 수익은 통화 공급의 지속적인 리베이스(rebase) 를 통해 OUSD 보유자에게 전달됩니다. OUSD는 프로토콜이 생성한 수익률에 따라 통화 공급을 지속적으로 조정합니다. 이를 통해 OUSD의 가격은 1달러로 고정되는 반면 토큰 보유자의 지갑 잔액은 프로토콜로 얻은 수익률을 반영하기 위해 실시간으로 조정됩니다.

결론적으로 OUSD는 사용하기 쉬우며, 자동으로 큰 수익을 제공하기에 기존 스테이블 코인 보다 보유시에 더 많은 이익을 제공하는 스테이블 코인입니다.

