# Panoramica

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD è costituito da una serie di smart contract. Ciascuno di questi contratti è racchiuso in un contratto delega che può essere aggiornato tramite i protocolli di governance.

Internamente, il possesso nella pool viene monitorata utilizzando un sistema di crediti che rappresenta la percentuale di possesso della pool per ciascun detentore. Il contratto ERC-20 gestisce la conversione in USD quando si visualizza un saldo o si inizia un trasferimento tra wallet.

Il Vault è responsabile del minting e del burning di OUSD. Inoltre, applica la percentuale di risorse da distribuire a ciascuna delle [Strategies](../core-concepts/supported-strategies/)supportate. To optimize gas costs, the vault maintains a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.



