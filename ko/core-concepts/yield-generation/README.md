# 이자 생산(Yield Generation)

**자동화 된 이자 농사(yield farming)**

새로운 대출 및 자동화된 시장 제조업체 풀의 폭발적인 증가로 인해 총 가치 잠금\(TVL\), 이 가속화되는 한편, 생산 농가들이 효율적이고 최적의 방식으로 자본을 수동으로 할당하는 것도 점점 더 어려워지고 있습니다.

[와이언(Yearn)](https://yearn.finance/) 은 스마트 컨트렉트가 다양한 전략에 걸쳐 자금 재조정을 자동화하여 대출이자, 시장 조성 수수료 및 보상 토큰을 최적으로 얻을 수 있음을 보여주었습니다. Over time, new strategies will be deployed that maximize returns while minimizing risk and dependencies.

![](../../.gitbook/assets/ousd_docs_graphics_1.png)

OUSD uses the following high-level strategies for generating yield:

{% page-ref page="lending.md" %}

{% page-ref page="market-making.md" %}

{% page-ref page="rewards.md" %}

OUSD is able to generate higher yields than competing protocols due to a combination of important design decisions that amplify the rewards that are returned to OUSD holders:

* Exit fees are returned to the pool, rewarding long term holders
* Price oracles favor the collective over the individual, again rewarding long term holders
* Smart contracts must manually opt-in to earn yield. This allows the protocol to put more capital to work than would be otherwise possible.
* Smart strategies balance risk and reward more effectively than deploying capital in any single underlying strategy.

