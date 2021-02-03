# Ribasamento & Smart Contract

Se stai utilizzando un wallet multi-sig o un altro smart contract che intende sincronizzarsi con i rebasamenti di OUSD, devi richiamare la funzione `rebaseOptIn()` dello smart contract di OUSD. Questo si deve fare solo con gli smart contract perché i wallet EOA vengono registrati automaticamente.

{% hint style="info" %}
I wallet multi-sig o altri smart contract devono richiamare la funzione ` rebaseOptIn()` per cominciare ad accumulare rendimento.
{% endhint %}

Una delle difficoltà che si ha sul ribasamento delle valute come OUSD, è che non funzionano molto bene con i market maker automatizzati \(AMM\) come Uniswap o Balancer. Questi exchange decentralizzati si basano sull'offerta e sulla domanda per determinare il prezzo degli asset scambiati. Questo crea confusioni matematiche quando l'ammontare di OUSD detenuto da uno smart contract cambia inaspettatamente a causa del nuovo rendimento generato.

In precedenza abbiamo aggiunto uno [smart contract](https://medium.com/originprotocol/upgrades-to-the-ousd-smart-contracts-deliver-higher-yield-and-better-uniswap-support-aa592e51d3f2) che richiamava la funzione ` sync()` di Uniswap ogni volta che venisse triggerata la funzione `rebase()` degli smart contract di OUSD. Sebbene ciò impedisse gli utenti di visualizzare brutti messaggi di errore quando cercavano di scambiare OUSD in Uniswap, ciò introduceva comunque delle perdite nel sistema. Dopo aver richiamato la funzione di sync, Uniswap rileva che nel vault ci sono più OUSD di USDT, e questo fa scendere il prezzo di OUSD erroneamente verso il basso rispetto a quello di USDT. Sebbene sia possibile contare sugli arbitraggi per il ribilanciamento del prezzo, è comunque preferibile evitare del tutto questa perdita. Dato il numero sempre crescente di AMM competitivi e fork di Uniswap, sarebbe diventato presto impossibile, per non parlare del costo del gas, provarli tutti e adeguarsi caso per caso.

Dopo molte discussioni, abbiamo deciso che la soluzione più scalabile fosse quella di aggiungere una iscrizione esplicita per gli smart contract, così che solo dopo essersi iscritti possano ricevere il rendimento tramite il meccanismo del ribasamento. Questo risolve il problema della fornitura sempre in espansione negli AMM pur consentendo comunque ai wallet multi-sig e anche ad altri smart contract, l'opportunità di continuare a partecipare e guadagnare rendimenti.

{% hint style="warning" %}
If you are deploying a contract and intend to call`rebaseOptIn()`to earn yield you cannot call it from the contracts constructor. The contract must be deployed before it can be called.
{% endhint %}

If you are using a multi-sig wallet like [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) or [Gnosis Safe](https://gnosis-safe.io/), you will need the  [proxy contract address for OUSD](../../smart-contracts/registry.md) and the corresponding [ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805). Once you add those, you will be able to call the `rebaseOptIn()` function to opt into receiving yield via rebasing or`rebaseOptOut()` to turn it off again.





