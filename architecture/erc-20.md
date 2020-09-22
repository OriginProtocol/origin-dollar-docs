# 概观

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD 由一系列智能合约组成。 每一个合约都被包在可以通过治理协议升级的代理合约中。

在内部，每个持有者池中的所有权百分比是用积分系统来跟踪。 在查看余额或启动钱包之间的转账时由 ERC-20 合约处理转换为美元的条款。

保险库（The Vault）负责铸造（minting）和燃烧（burning）OUSD。 它也会强制部署到每个受支持的 [策略](../core-concepts/supported-strategies/)的资产百分比。 为了优化gas成本，保险库保留了一个缓冲区以允许大多数存款和赎回都可以在无需从策略中存入/清算资产的情况下发生。



