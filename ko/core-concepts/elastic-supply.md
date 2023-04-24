# 공급 탄력성(Elastic Supply)

**공급 탄력성. 안정적 가격.**

OUSD는 대부분의 토큰과 다르게 작동합니다. 관리 대상 자산의 가치가 증가함에 따라 가격이 상승하는 대신 \ (컴파운드의 c토큰 또는 와이언의 y토큰 \) 1 개의 OUSD의 가치는 약 $ 1로 일정하게 유지됩니다. 대신, 컨트랙트는 지속적으로 화폐 공급을 조정하고 모든 토큰 보유자의 지갑에있는 잔액을 자동으로 업데이트하여 프로토콜로 얻은 수익률을 반영합니다.

{% hint style="info" %}
은행 계좌에서 발생하는 이자로 생각하면 됩니다. 미국 달러의 계정 단위와 가치는 변경되지 않습니다. 이자를 받으면 시간이 지남에 따라 더 많은 미국 달러를 받게됩니다.
{% endhint %}

![](../.gitbook/assets/ousd_docs_graphics_4.png)

이 메커니즘은 [앰플포스(Ampleforth)](https://www.ampleforth.org/)의해 취해진 새로운 접근 방식에서 영감을 얻었지만 강조 할 가치가있는 몇 가지 주요 차이점이 있습니다.

1. OUSD는 100 % 다른 스테이블 코인에 의해 뒷받침되며 달러에 대한 페그(peg) 를 유지하는 것과 같은 문제가 없습니다. OUSD를 쉽게 채굴하고 상환 할 수 있다는 점을 감안할 때, 우리는 페그가 유지되도록 중재자를 의지할 수 있습니다.
2. OUSD rebasing should only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Any decrease in your balance would be an indication of trouble in the system.
3. 하루에 한 번 리베이스하는 앰플포스와 달리, OUSD의 통화 공급은 수익률이 생성됨에 따라 실시간으로 지속적으로 업데이트됩니다.

