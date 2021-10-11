# Timelock

{% hint style="danger" %}
The timelock has been added but is currently set to 1 minute. This allows for a faster response if any critical issues are discovered. The timelock is governed by Origin's 5 of 8 multi-sig.
{% endhint %}

Il contratto timelock applica un periodo di attesa di 48 ore prima che qualsiasi modifica ai contratti OUSD possano essere eseguiti. Il timelock può essere chiamato dal nostro multi-sig ed è il proprietario dei nostri contratti [ERC-20](../architecture.md),[Vault](vault.md), e [Strategie](strategies.md). Le azioni di amministrazione ritardate offrono agli utenti la possibilità di uscire da OUSD se i suoi amministratori diventassero malevoli, se venissero compromessi o se apportassero una modifica non gradita agli utenti.

{% hint style="info" %}
Il timelock è una misura di sicurezza che offre 48 ore ai titolari di OUSD per ritirare i propri fondi se dovessero avere obiezioni a qualsiasi aggiornamento proposto al protocollo.
{% endhint %}

OUSD utilizza una versione leggermente modificata di [Compound Timelock](https://compound.finance/docs/governance) che è stata [verificata da OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). The two notable differences are:

1. OUSD will initially use a shorter wait period (48 hours) than Compound (72 hours) to allow for a faster response if any issues are discovered.
2. Some actions, such a reallocating funds between existing strategies and freezing deposits can be called immediately without requiring the 48 waiting period. This is in case a major vulnerability is discovered.



