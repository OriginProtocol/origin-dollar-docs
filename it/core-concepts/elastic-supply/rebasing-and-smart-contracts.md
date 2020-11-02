# Ribasamento & Smart Contract

Se stai utilizzando un wallet multi-sig o un altro smart contract che intende sincronizzarsi con i rebasamenti di OUSD, devi richiamare la funzione `rebaseOptIn()` dello smart contract di OUSD. Questo si deve fare solo con gli smart contract perché i wallet EOA vengono registrati automaticamente.

{% hint style="info" %}
I wallet multi-sig o altri smart contract devono richiamare la funzione ` rebaseOptIn()` per cominciare ad accumulare rendimento.
{% endhint %}

Una delle difficoltà che si ha sul ribasamento delle valute come OUSD, è che non funzionano molto bene con i market maker automatizzati \(AMM\) come Uniswap o Balancer. Questi exchange decentralizzati si basano sull'offerta e sulla domanda per determinare il prezzo degli asset scambiati. Questo crea confusioni matematiche quando l'ammontare di OUSD detenuto da uno smart contract cambia inaspettatamente a causa del nuovo rendimento generato.

In precedenza abbiamo aggiunto uno [smart contract](https://medium.com/originprotocol/upgrades-to-the-ousd-smart-contracts-deliver-higher-yield-and-better-uniswap-support-aa592e51d3f2) che richiamava la funzione ` sync()` di Uniswap ogni volta che venisse triggerata la funzione `rebase()` degli smart contract di OUSD. Sebbene ciò impedisse gli utenti di visualizzare brutti messaggi di errore quando cercavano di scambiare OUSD in Uniswap, ciò introduceva comunque delle perdite nel sistema. After calling sync, Uniswap detects that there is more OUSD than USDT in the pool, which incorrectly pushes down the price of OUSD relative to USDT. While we can count on arbitrageurs to correct the price, it’s better if we can avoid this loss altogether. Given the ever-growing number of competitive AMM’s and forks of Uniswap, it would quickly become infeasible, not to mention gas-expensive, to try and special-case all of them.

After much discussion, we decided that the most scalable solution was to make smart contracts explicitly opt-in to receiving yield via the rebasing mechanism. This fixes the issue with the expanding supply on AMM’s while still allowing multi-sig wallets and other smart contracts the opportunity to still participate and earn yield.

If you are using a multi-sig wallet like [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) or [Gnosis Safe](https://gnosis-safe.io/), you will need the [ABI ](https://api.etherscan.io/api?module=contract&action=getabi&address=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)and contract address \(0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86\) for OUSD. Once you add those, you will be able to call the `rebaseOptIn()` function to opt into receving yield via rebasing or`rebaseOptOut()` to turn it off again.

