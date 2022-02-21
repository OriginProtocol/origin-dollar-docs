# 아키텍처(Architecture)

![](../.gitbook/assets/ousd\_docs\_graphics\_3.png)

OUSD는 일련의 스마트 컨트렉트로 구성됩니다. 이러한 각 계약은 거버넌스 프로토콜을 통해 업그레이드 할 수 있는 프록시 계약으로 포장됩니다.

Internally, ownership in the vault is tracked using a credits system that represents the percent ownership of the vault for each holder. The [ERC-20](api/erc-20-1.md) contract handles the conversion to USD terms when viewing a balance or initiating a transfer between wallets.

The [Vault](api/vault.md) is responsible for minting and burning OUSD. 또한 지원되는 각 [전략 ](../core-concepts/supported-strategies/)에 배포되는 자산의 비율도 적용합니다. 가스 비용 최적화를 위해, 금고(Vault) 는 대부분의 예금 및 상환이 전략에서 자산을 감거나 풀지 않고 발생할 수 있도록 버퍼를 유지합니다.

The Flipper is a smart contract for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. This contract is used as an alternative way to route user transactions originating from the web app. It's important to note that this contract may become bankrupt on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Flipper uses around 45% less gas than Uniswap v3 due to its simplicity.

