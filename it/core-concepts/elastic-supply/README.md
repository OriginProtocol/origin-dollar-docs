# Elastic Supply

**Fornitura elastica. Prezzo stabile.**

OUSD funziona differentemente dalla maggior parte dei token. Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. Instead, the contracts constantly adjust the monetary supply and automatically updates the balance in every token holder’s wallet to reflect the yield that has been earned by the protocol.&#x20;

{% hint style="info" %}
Pensalo come un interesse maturato sul conto in banca. L'unità per il conto e il valore del Dollaro Statunitense non cambia. Ottieni più dollari statunitensi nel tempo, a mano a mano che guadagni interessi.
{% endhint %}

![](../../.gitbook/assets/ousd\_docs\_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD è supportato al 100% da altre stablecoin e non ha il problema di mantenersi ancorato al dollaro. Given the ease of minting and redeeming OUSD, we can count on arbitrageurs to ensure the peg is maintained.&#x20;
2. Il ribasamento di OUSD aumenterà solo l'offerta poiché la quantità di OUSD coniati è legata ai guadagni realizzati guadagnati dalle strategie sottostanti. Il tuo capitale è protetto fintanto che va tutto bene con i protocolli di prestito/AMM e stablecoin. Il tuo saldo OUSD non diminuirà mai, ma il valore potrebbe calare se si verificasse un problema nei sistemi sottostanti.
3. Unlike Ampleforth, which only rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. I ribasamenti vengono innescati regolarmente quando gli utenti interagiscono con gli smart contract di OUSD. Chainlink Keepers ensure at least one rebase occurs every day.

**Innesco manuale di un ribasamento**

Chiunque può innescare un ribasamento in qualsiasi momento semplicemente [richiamando la funzione di rebase nel vault](https://etherscan.io/address/originvault.eth#writeProxyContract). Puoi farlo su Etherscan connettendo un wallet web3.
