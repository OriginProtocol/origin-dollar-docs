# Architettura

![](../.gitbook/assets/ousd_docs_graphics\_3.png)

OUSD è costituito da una serie di smart contract. Ciascuno di questi contratti è racchiuso in un contratto proxy che può essere migliorato tramite i protocolli di governance.

Internamente, la proprietà del vault è monitorata attraverso un sistema a crediti, i quali rappresentano la percentuale di proprietà del vault posseduta da ciascun holder. Il contratto [ERC-20](api/erc-20-1.md) gestisce la conversione in USD quando si visualizza un saldo o si inizia un trasferimento tra wallet.

Il [Vault](api/vault.md) è responsabile della coniazione (minting) e della distruzione (burning) degli OUSD. Inoltre, applica la percentuale di risorse che sono rilasciate in ciascuna delle [Strategies](../core-concepts/supported-strategies/) supportate. Per ottimizzare i costi del gas, il vault mantiene un buffer per consentire alla maggior parte dei depositi e dei rimborsi, di avvenire senza liquidare/sciogliere asset dalle strategie.

OUSD Swap, aka "Flipper" is a smart contract that is provided by Origin for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. This contract is used as an alternative way to route user transactions originating from the web app. It's important to note that this contract may become bankrupt on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Origin Swap uses around 45% less gas than Uniswap v3 due to its simplicity.

