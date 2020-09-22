# 架构

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD 由一系列智能合约组成。 每一个合约都被包在可以通过治理协议升级的代理合约中。

在内部，每个持有者池中的所有权百分比是用积分系统来跟踪。 The [ERC-20](api/erc-20-1.md) contract handles the conversion to USD terms when viewing a balance or initiating a transfer between wallets.

The [Vault](api/vault.md) is responsible for minting and burning OUSD. 它也会强制部署到每个受支持的 [策略](../core-concepts/supported-strategies/)的资产百分比。 为了优化gas成本，保险库保留了一个缓冲区以允许大多数存款和赎回都可以在无需从策略中存入/清算资产的情况下发生。



