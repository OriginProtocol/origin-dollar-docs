# Elastic Supply

**Fornitura elastica. Prezzo stabile.**

OUSD funziona differentemente dalla maggior parte dei token. Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. Invece, gli smart contract regolano costantemente l'offerta monetaria e aggiorna automaticamente il saldo nel portafoglio di ogni token holder per riflettere il rendimento che è stato guadagnato dal protocollo.

{% hint style="info" %}
Pensalo come un interesse maturato sul conto in banca. L'unità per il conto e il valore del Dollaro Statunitense non cambia. Ottieni più dollari statunitensi nel tempo, a mano a mano che guadagni interessi.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD è supportato al 100% da altre stablecoin e non ha il problema di mantenersi ancorato al dollaro. Data la facilità di generazione e di riscatto degli OUSD, possiamo contare sulla presenza degli arbitraggisti per garantire l'ancoraggio.
2. Il ribasamento di OUSD aumenterà solo l'offerta poiché la quantità di OUSD coniati è legata ai guadagni realizzati guadagnati dalle strategie sottostanti. Il tuo capitale è protetto fintanto che va tutto bene con i protocolli di prestito/AMM e stablecoin. Il tuo saldo OUSD non diminuirà mai, ma il valore potrebbe calare se si verificasse un problema nei sistemi sottostanti.
3. A differenza di Ampleforth, che fa il ribasamento una volta al giorno, l'offerta monetaria di OUSD è aggiornata costantemente in tempo reale a mano a mano che viene generato il rendimento. I ribasamenti vengono innescati regolarmente quando gli utenti interagiscono con gli smart contract di OUSD.

**Innesco manuale di un ribasamento**

Chiunque può innescare un ribasamento in qualsiasi momento semplicemente [richiamando la funzione di rebase nel vault](https://etherscan.io/address/originvault.eth#writeProxyContract). Puoi farlo su Etherscan connettendo un wallet web3.
