# Architecture

![](../.gitbook/assets/ousd_docs_graphics\_3.png)

OUSD is made up of a series of smart contracts. Each of these contracts is wrapped in a proxy contract that can be upgraded via the governance protocols.

Internally, ownership in the vault is tracked using a credits system that represents the percent ownership of the vault for each holder. The [ERC-20](api/erc-20-1.md) contract handles the conversion to USD terms when viewing a balance or initiating a transfer between wallets.

The [Vault](api/vault.md) is responsible for minting and burning OUSD. It also enforces the percentage of assets that are deployed to each of the supported [Strategies](../core-concepts/supported-strategies/). To optimize gas costs, the vault maintains a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.

OUSD Swap, aka "Flipper" is a smart contract that is provided by Origin for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. This contract is used as an alternative way to route user transactions originating from the web app. It's important to note that this contract may become bankrupt on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Origin Swap uses around 45% less gas than Uniswap v3 due to its simplicity.

