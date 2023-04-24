# Timelock

{% hint style="danger" %}
Il timelock verrà aggiunto subito dopo che tutto sia verificato come funzionante. Fino ad allora, la governance dei contratti rimarrà in mano a 5 di 8 multi-sig di Origin. Questo permette una più immediata risposta verso qualsiasi problematica che possa venir scoperta.
{% endhint %}

Il contratto timelock applica un periodo di attesa di 48 ore prima che qualsiasi modifica ai contratti OUSD possano essere eseguiti. Il timelock può essere chiamato dal nostro multi-sig ed è il proprietario dei nostri contratti [ERC-20](../architecture.md),[Vault](vault.md), e [Strategie](strategies.md). Le azioni di amministrazione ritardate offrono agli utenti la possibilità di uscire da OUSD se i suoi amministratori diventano malevoli, se vengono compromessi o apportano una modifica che agli utenti non piace.

{% hint style="info" %}
Il blocco temporale è una misura di sicurezza che offre ai titolari di OUSD 48 ore per ritirare i propri fondi se dovessero avere obiezioni a qualsiasi aggiornamento proposto al protocollo.
{% endhint %}

OUSD utilizza una versione leggermente modificata di [Compound Timelock](https://compound.finance/docs/governance) che è stata [verificata da OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). Le 3 differenze importanti sono:

1. OUSD inizialmente utilizzerà un periodo di attesa più breve \(48 ore\) rispetto a quello di Compund \(72 ore\), per permettere una più rapida risposta a qualsiasi tipo di problema riscontrato.
2. Una volta che le 48 ore saranno passate, chiunque sarà libero di eseguire le chiamate, e non più solo il proprietario del contratto.
3. I depositi \(ma non i ritiri o i trasferimenti\) potranno essere immediatamente congelati senza richiedere il periodo di attesa di 48 ore. Questo è nel caso in cui venga scoperta una grave vulnerabilità.





