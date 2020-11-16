# Ribasamento & Smart Contract

Se stai utilizzando un wallet multi-sig o un altro smart contract che intende sincronizzarsi con i rebasamenti di OUSD, devi richiamare la funzione `rebaseOptIn()` dello smart contract di OUSD. Questo si deve fare solo con gli smart contract perché i wallet EOA vengono registrati automaticamente.

{% hint style="info" %}
I wallet multi-sig o altri smart contract devono richiamare la funzione ` rebaseOptIn()` per cominciare ad accumulare rendimento.
{% endhint %}

Una delle difficoltà che si ha sul ribasamento delle valute come OUSD, è che non funzionano molto bene con i market maker automatizzati \(AMM\) come Uniswap o Balancer. Questi exchange decentralizzati si basano sull'offerta e sulla domanda per determinare il prezzo degli asset scambiati. Questo crea confusioni matematiche quando l'ammontare di OUSD detenuto da uno smart contract cambia inaspettatamente a causa del nuovo rendimento generato.

In precedenza abbiamo aggiunto uno [smart contract](https://medium.com/originprotocol/upgrades-to-the-ousd-smart-contracts-deliver-higher-yield-and-better-uniswap-support-aa592e51d3f2) che richiamava la funzione ` sync()` di Uniswap ogni volta che venisse triggerata la funzione `rebase()` degli smart contract di OUSD. Sebbene ciò impedisse gli utenti di visualizzare brutti messaggi di errore quando cercavano di scambiare OUSD in Uniswap, ciò introduceva comunque delle perdite nel sistema. After calling sync, Uniswap detects that there is more OUSD than USDT in the vault, which incorrectly pushes down the price of OUSD relative to USDT. Sebbene sia possibile contare sugli arbitraggi per il ribilanciamento del prezzo, è comunque preferibile evitare del tutto questa perdita. Dato il numero sempre crescente di AMM competitivi e fork di Uniswap, sarebbe diventato presto impossibile, per non parlare del costo del gas, provarli tutti e adeguarsi caso per caso.

Dopo molte discussioni, abbiamo deciso che la soluzione più scalabile fosse quella di aggiungere una iscrizione esplicita per gli smart contract, così che solo dopo essersi iscritti possano ricevere il rendimento tramite il meccanismo del ribasamento. Questo risolve il problema della fornitura sempre in espansione negli AMM pur consentendo comunque ai wallet multi-sig e anche ad altri smart contract, l'opportunità di continuare a partecipare e guadagnare rendimenti.

Se stai utilizzando un wallet multi-sig come [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) oppure [Gnosis Safe](https://gnosis-safe.io/), avrai bisogno dell'ultimo [address di implementazione relativo a OUSD](../../smart-contracts/registry.md) e il corrispettivo [ ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805). Una volta che li avrai aggiunti, sarai in grado di richiamare la funzione `rebaseOptIn()` per iscriverti alla ricezione del rendimento tramite il ribasamento o tramite il richiamo della funzione `rebaseOptOut()` per disattivarlo nuovamente.

{% hint style="warning" %}
Se stai rilasciando un contratto e intendi richiamare la funzione `rebaseOptin()` per guadagnare lo yield, non puoi richiamarla dal costruttore degli smart contract. Lo smart contract deve essere rilasciato prima di poter essere richiamato.
{% endhint %}

[ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)

