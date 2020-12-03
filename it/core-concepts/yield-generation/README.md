# Generare Yield

**Yield farming automatizzato**

Mentre l'esplosione di Cambrian dei nuovi pool di prestiti e market making automatizzati ha alimentato il valore totale bloccato \(TVL\), allo stesso tempo ha anche fatto sì che diventasse sempre più difficile allocare manualmente il capitale in modi efficienti e ottimali per i procacciatori di yield.

[Yearn](https://yearn.finance/) ha dimostrato che gli smart contract possono automatizzare il ribilanciamento dei fondi attraverso varie strategie per guadagnare in modo ottimizzato: interessi di prestito, commissioni di market making e token di ricompensa. Over time, new strategies will be deployed that maximize returns while minimizing risk and dependencies.

![](../../.gitbook/assets/ousd_docs_graphics_1.png)

OUSD uses the following high-level strategies for generating yield:

{% page-ref page="lending.md" %}

{% page-ref page="market-making.md" %}

{% page-ref page="rewards.md" %}

OUSD is able to generate higher yields than competing protocols due to a combination of important design decisions that amplify the rewards that are returned to OUSD holders:

* Exit fees are returned to the pool, rewarding long term holders
* Price oracles favor the collective over the individual, again rewarding long term holders
* Smart contracts must manually opt-in to earn yield. This allows the protocol to put more capital to work than would be otherwise possible.
* Smart strategies balance risk and reward more effectively than deploying capital in any single underlying strategy.

