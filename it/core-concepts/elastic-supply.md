# Elastic Supply

**Fornitura elastica. Prezzo stabile.**

OUSD funziona differentemente dalla maggior parte dei token. Invece di aumentare il prezzo all'aumentare del valore degli asset in gestione \(come con i cToken di Compound o i yToken di Yearn\), il valore di un OUSD rimane costante e approssimato a 1$. Invece, gli smart contract regolano costantemente l'offerta monetaria e aggiorna automaticamente il saldo nel portafoglio di ogni token holder per riflettere il rendimento che è stato guadagnato dal protocollo.

{% hint style="info" %}
Pensalo come un interesse maturato sul conto in banca. The unit of account and value for the US dollar doesn’t change. Ottieni più dollari statunitensi nel tempo, a mano a mano che guadagni interessi.
{% endhint %}

![](../.gitbook/assets/ousd_docs_graphics_4.png)

Questo meccanismo è stato ispirato dal nuovo approccio adottato da [ Ampleforth](https://www.ampleforth.org/), ma ci sono alcune differenze chiave che vale la pena evidenziare:

1. OUSD è supportato al 1''% da stablecoin e non avrà il problema di mantenersi ancorato al dollaro. Data la facilità di generazione e di riscatto degli OUSD, possiamo contare sulla presenza degli arbitraggisti per garantire l'ancoraggio.
2. OUSD rebasing should only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Any decrease in your balance would be an indication of trouble in the system.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated.

