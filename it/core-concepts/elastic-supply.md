# Elastic Supply

**Fornitura elastica. Prezzo stabile.**

OUSD funziona differentemente dalla maggior parte dei token. Invece di aumentare il prezzo all'aumentare del valore degli asset in gestione \(come con i cToken di Compound o i yToken di Yearn\), il valore di un OUSD rimane costante e approssimato a 1$. Invece, gli smart contract regolano costantemente l'offerta monetaria e aggiorna automaticamente il saldo nel portafoglio di ogni token holder per riflettere il rendimento che è stato guadagnato dal protocollo.

{% hint style="info" %}
Pensalo come un interesse maturato sul conto in banca. L'unità per il conto e il valore del Dollaro Statunitense non cambia. Ottieni più dollari statunitensi nel tempo, a mano a mano che guadagni interessi.
{% endhint %}

![](../.gitbook/assets/ousd_docs_graphics_4.png)

Questo meccanismo è stato ispirato dal nuovo approccio adottato da [ Ampleforth](https://www.ampleforth.org/), ma ci sono alcune differenze chiave che vale la pena evidenziare:

1. OUSD è supportato al 1''% da stablecoin e non avrà il problema di mantenersi ancorato al dollaro. Data la facilità di generazione e di riscatto degli OUSD, possiamo contare sulla presenza degli arbitraggisti per garantire l'ancoraggio.
2. Il ribasamento di OUSD dovrebbe solo aumentare l'offerta poiché la quantità di OUSD coniati è legata ai guadagni realizzati guadagnati dalle strategie sottostanti. Il tuo capitale è protetto fintanto che va tutto bene con i protocolli di prestito/AMM e stablecoin. Qualsiasi calo del saldo sarebbe un indicazione di problemi nel sistema.
3. A differenza di Ampleforth, che fa il ribasamento una volta al giorno, l'offerta monetaria di OUSD è aggiornata costantemente in tempo reale a mano a mano che viene generato il rendimento.

