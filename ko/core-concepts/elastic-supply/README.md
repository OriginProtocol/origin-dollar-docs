# 공급 탄력성(Elastic Supply)

**공급 탄력성. 안정적 가격.**

OUSD는 대부분의 토큰과 다르게 작동합니다. 관리 대상 자산의 가치가 증가함에 따라 가격이 상승하는 대신 \ (컴파운드의 c토큰 또는 와이언의 y토큰 \) 1 개의 OUSD의 가치는 약 $ 1로 일정하게 유지됩니다. 대신, 컨트랙트는 지속적으로 화폐 공급을 조정하고 모든 토큰 보유자의 지갑에있는 잔액을 자동으로 업데이트하여 프로토콜로 얻은 수익률을 반영합니다.

{% hint style="info" %}
은행 계좌에서 발생하는 이자로 생각하면 됩니다. 미국 달러의 계정 단위와 가치는 변경되지 않습니다. 이자를 받으면 시간이 지남에 따라 더 많은 미국 달러를 받게됩니다.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

이 메커니즘은 [앰플포스(Ampleforth)](https://www.ampleforth.org/)의해 취해진 새로운 접근 방식에서 영감을 얻었지만 강조 할 가치가있는 몇 가지 주요 차이점이 있습니다.

1. OUSD is 100% backed by other stablecoins and does not have the same challenge maintaining the peg to the dollar. OUSD를 쉽게 채굴하고 상환 할 수 있다는 점을 감안할 때, 우리는 페그가 유지되도록 중재자를 의지할 수 있습니다.
2. OUSD rebasing will only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Your OUSD balance will never decrease, but the value could drop if there's a failure in the underlying systems.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebases are triggered regularly as users interact with the OUSD contracts.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.

