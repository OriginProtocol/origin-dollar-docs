# 아키텍처(Architecture)

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD는 일련의 스마트 컨트렉트로 구성됩니다. 이러한 각 계약은 거버넌스 프로토콜을 통해 업그레이드 할 수 있는 프록시 계약으로 포장됩니다.

내부적으로 풀(pool) 의 소유권은 각 홀더에 대한 풀의 소유권 비율을 나타내는 크레딧 시스템을 사용하여 추적됩니다. The [ERC-20](api/erc-20-1.md) contract handles the conversion to USD terms when viewing a balance or initiating a transfer between wallets.

The [Vault](api/vault.md) is responsible for minting and burning OUSD. 또한 지원되는 각 [전략 ](../core-concepts/supported-strategies/)에 배포되는 자산의 비율도 적용합니다. 가스 비용 최적화를 위해, 금고(Vault) 는 대부분의 예금 및 상환이 전략에서 자산을 감거나 풀지 않고 발생할 수 있도록 버퍼를 유지합니다.



