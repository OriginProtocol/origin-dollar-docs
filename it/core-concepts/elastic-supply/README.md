# Elastic Supply

**Fornitura elastica. Prezzo stabile.**

OUSD funziona differentemente dalla maggior parte dei token. Invece di aumentare il prezzo all'aumentare del valore degli asset in gestione \(come con i cToken di Compound o i yToken di Yearn\), il valore di un OUSD rimane costante e approssimato a 1$. Invece, gli smart contract regolano costantemente l'offerta monetaria e aggiorna automaticamente il saldo nel portafoglio di ogni token holder per riflettere il rendimento che è stato guadagnato dal protocollo.

{% hint style="info" %}
Pensalo come un interesse maturato sul conto in banca. L'unità per il conto e il valore del Dollaro Statunitense non cambia. Ottieni più dollari statunitensi nel tempo, a mano a mano che guadagni interessi.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

Questo meccanismo è stato ispirato dal nuovo approccio adottato da [ Ampleforth](https://www.ampleforth.org/), ma ci sono alcune differenze chiave che vale la pena evidenziare:

1. OUSD è supportato al 100% da altre stablecoin e non ha il problema di mantenersi ancorato al dollaro. Data la facilità di generazione e di riscatto degli OUSD, possiamo contare sulla presenza degli arbitraggisti per garantire l'ancoraggio.
2. OUSD rebasing will only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Il tuo capitale è protetto fintanto che va tutto bene con i protocolli di prestito/AMM e stablecoin. Your OUSD balance will never decrease, but the value could drop if there's a failure in the underlying systems.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebases are triggered regularly as users interact with the OUSD contracts.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.

