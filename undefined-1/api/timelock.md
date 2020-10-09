# 타임락\(TimeLock\)

{% hint style="danger" %}
타임락\(TimeLock\)은 모든 기능이 정상적으로 잘 작동하는 것이 확인되면 곧 추가될 것입니다. 그때까지 계약은 오리진의 8 멀티-시그 중 5에 의해 관리됩니다. 따라서 중요한 문제가 발견될 경우 보다 신속하게 대응할 수 있습니다.
{% endhint %}

타임락\(Timelock\) 컨트렉트 OUSD 계약에 대한 변경 사항이 실행될 때까지 48시간의 대기 기간을 적용 받습니다. 타임은 멀티시그로 호출할 수 있으며 오리진의 [ERC-20](../architecture.md), 금고\([Vault](vault.md)\), 그리고 전략\( [Strategies](strategies.md)\) 컨트렉트의 소유자입니다. 시간 지연 관리 작업을 사용하면 관리자가 악의적으로 진행된 프로세스로인한 손상에 또 사용자가 원하지 않는 변경을 수행할 경우 OUSD를 종료할 수 있습니다.

{% hint style="info" %}
타임락\(Timelock\)은 OUSD 보유자가 제안된 프로토콜 업그레이드에 대해 이의를 제기할 경우 자금을 회수할 수 있는 48시간을 제공하는 안전 조치입니다.
{% endhint %}

OUSD는 오픈제플린\([audited by OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/)\)이 감사한 컴파운드 타임락\([Compound Timelock](https://compound.finance/docs/governance)\)에서 약간 수정된 버전을 사용하고 있습니다. 세 가지 주목할 만한 차이점은 다음과 같습니다:

1. OUSD는 처음에 복합\(72시간\)보다 짧은 대기 시간\(48시간\)을 사용하여 문제가 발견될 경우 더 빠른 응답을 허용합니다. 
2. 48시간이 지나면 계약 소유자뿐만 아니라 누구나 자유롭게 통화를 실행할 수 있습니다. 
3. 예금\(하지만 인출 또는 이체할 수 없음\)은 48개의 대기 기간 없이 즉시 동결될 수 있습니다. 이는 주요 취약성이 발견된 경우에 해당합니다.

