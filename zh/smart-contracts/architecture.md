# 架构

![](../.gitbook/assets/ousd\_docs\_graphics\_3.png)

OUSD 由一系列智能合约组成。 每一个合约都被包在可以通过治理协议升级的代理合约中。

Internally, ownership in the vault is tracked using a credits system that represents the percent ownership of the vault for each holder. 在查看余额或启动钱包之间的转账时由 [ERC-20](api/erc-20-1.md) 合约处理转换为美元的条款。

[保险库（Vault）](api/vault.md) 负责铸造和燃烧OUSD。 它也会强制部署到每个受支持的 [策略](../core-concepts/supported-strategies/)的资产百分比。 为了优化gas成本，保险库保留了一个缓冲区以允许大多数存款和赎回都可以在无需从策略中存入/清算资产的情况下发生。

The Flipper is a smart contract for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. This contract is used as an alternative way to route user transactions originating from the web app. It's important to note that this contract may become bankrupt on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Flipper uses around 45% less gas than Uniswap v3 due to its simplicity.

