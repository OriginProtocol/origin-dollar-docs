# Panoramica

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD è costituito da una serie di smart contract. Ciascuno di questi contratti è racchiuso in un contratto delega che può essere aggiornato tramite i protocolli di governance.

Internamente, il possesso nella pool viene monitorata utilizzando un sistema di crediti che rappresenta la percentuale di possesso della pool per ciascun detentore. The ERC-20 contract handles the conversion to USD terms when viewing a balance or initiating a transfer between wallets.

The Vault is responsible for minting and burning OUSD. It also enforces the percentage of assets that are deployed to each of the supported [Strategies](../core-concepts/supported-strategies/). To optimize gas costs, the vault maintains a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.



