# 架构

![](../.gitbook/assets/ousd\_docs\_graphics\_3.png)

OUSD 由一系列智能合约组成。 每一个合约都被包在可以通过治理协议升级的代理合约中。

Internally, ownership in the vault is tracked using a credits system that represents the percent ownership of the vault for each holder. 在查看余额或启动钱包之间的转账时由 [ERC-20](api/erc-20-1.md) 合约处理转换为美元的条款。

[保险库（Vault）](api/vault.md) 负责铸造和燃烧OUSD。 它也会强制部署到每个受支持的 [策略](../core-concepts/supported-strategies/)的资产百分比。 To optimize gas costs, the vault may maintain a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.

The Flipper is a smart contract for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. This contract is used as an alternative way to route user transactions originating from the web app. It's important to note that this contract may be empty on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Flipper uses around 45% less gas than Uniswap v3 due to its simplicity.

The Harvester contract collects reward tokens earned by the strategies, sells them, and sends the resulting stablecoins to the Dripper to be released to the vault. Anyone can call the harvest and earn 1% of the resulting USDT for doing so. This creates a self-incentivizing system that operates at a known fixed cost. See our [incentivized-harvesting-guide.md](../guides/incentivized-harvesting-guide.md "mention") for details.

The Dripper contract buffers aproximately one week of reward token sales proceeds and makes it avaiable at a smooth rate to the vault. This keeps OUSD yield from being extremely spiky when harvests come in. The rate is recalculated at least once per day and is the rate that it would take to distribute the current dripper holdings out over a one week period.



