# Architecture

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD is made up of a series of smart contracts. Each of these contracts is wrapped in a proxy contract that can be upgraded via the governance protocols.

Internally, ownership in the vault is tracked using a credits system that represents the percent ownership of the vault for each holder. The [ERC-20](api/erc-20-1.md) contract handles the conversion to USD terms when viewing a balance or initiating a transfer between wallets.

The [Vault](api/vault.md) is responsible for minting and burning OUSD. It also enforces the percentage of assets that are deployed to each of the supported [Strategies](../core-concepts/supported-strategies/). To optimize gas costs, the vault maintains a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.


