# Architettura

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD è costituito da una serie di smart contract. Ciascuno di questi contratti è racchiuso in un contratto proxy che può essere migliorato tramite i protocolli di governance.

Internamente, la proprietà del vault è monitorata attraverso un sistema a crediti, i quali rappresentano la percentuale di proprietà del vault posseduta da ciascun holder. Il contratto [ERC-20](api/erc-20-1.md) gestisce la conversione in USD quando si visualizza un saldo o si inizia un trasferimento tra wallet.

Il [Vault](api/vault.md) è responsabile della coniazione (minting) e della distruzione (burning) degli OUSD. Inoltre, applica la percentuale di risorse che sono rilasciate in ciascuna delle [Strategies](../core-concepts/supported-strategies/) supportate. Per ottimizzare i costi del gas, il vault mantiene un buffer per consentire alla maggior parte dei depositi e dei rimborsi, di avvenire senza liquidare/sciogliere asset dalle strategie.



