# 개요

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD는 일련의 스마트 컨트렉트로 구성됩니다. 이러한 각 계약은 거버넌스 프로토콜을 통해 업그레이드할 수 있는 프록시 계약으로 포장됩니다.

내부적으로 풀의 소유권은 각 홀더에 대한 풀의 소유권 비율을 나타내는 크레딧 시스템을 사용하여 추적됩니다. The ERC-20 contract handles the conversion to USD terms when viewing a balance or initiating a transfer between wallets.

The Vault is responsible for minting and burning OUSD. It also enforces the percentage of assets that are deployed to each of the supported [Strategies](../core-concepts/supported-strategies/). To optimize gas costs, the vault maintains a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.



