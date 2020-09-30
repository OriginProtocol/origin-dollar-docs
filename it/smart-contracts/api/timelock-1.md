# Timelock

{% hint style="danger" %}
Il timelock verrà aggiunto subito dopo che tutto sia verificato come funzionante. Fino ad allora, la governance dei contratti rimarrà in mano a 5 di 8 multi-sig di Origin. Questo permette una più immediata risposta verso qualsiasi problematica che possa venir scoperta.
{% endhint %}

Il contratto timelock applica un periodo di attesa di 48 ore prima che qualsiasi modifica ai contratti OUSD possano essere eseguiti. Il timelock può essere chiamato dal nostro multi-sig ed è il proprietario dei nostri contratti [ERC-20](../architecture.md),[Vault](vault.md), e [Strategie](strategies.md). Le azioni di amministrazione ritardate offrono agli utenti la possibilità di uscire da OUSD se i suoi amministratori diventano malevoli, se vengono compromessi o apportano una modifica che agli utenti non piace.

{% hint style="info" %}
The timelock is a safety measure that gives OUSD holders 48 hours to withdraw their funds if they have objections to any proposed upgrades to the protocol.
{% endhint %}

OUSD is using a slightly modified version of the [Compound Timelock](https://compound.finance/docs/governance) which has been [audited by OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). The 3 notable differences are:

1. OUSD will initially use a shorter wait period \(48 hours\) than Compound \(72 hours\) to allow for a faster response if any issues are discovered.
2. Once the 48 hours have passed, anyone is free to execute the call, not just the owner of the contract.
3. Deposits \(but not withdrawals or transfers\) can be immediately frozen without requiring the 48 waiting period. This is in case a major vulnerability is discovered.





