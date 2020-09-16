# Overview

OUSD is made up of a series of smart contracts. Each of these contracts is wrapped in a proxy contract that can be upgraded via governance. 

Internally, ownership of the pool is tracked using a credits system that represents the percent ownership of the pool for each holder. The ERC-20 contract handles the conversion to USD terms when viewing a balance or initiating a transfer between wallets.

The Vault is responsible for minting and burning OUSD. It also enforces what percentage of assets are deployed to each of the supported Strategies. 

To optimize gas costs, the vault maintains a buffer to allow deposits and redemptions without winding/unwinding assets from a Strategy. 

![](../.gitbook/assets/ousd_docs_graphics_3.png)



