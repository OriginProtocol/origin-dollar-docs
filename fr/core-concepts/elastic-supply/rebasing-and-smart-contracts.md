# Rebasement & Contrats intelligents

Si vous utilisez un portefeuille à signature multiples ou un autre contrat intelligent et que vous souhaitez participer au rebasement de OUSD, vous devez appeler la fonction `rebaseOptIn()`. Ceci s'applique seulement aux contrats intelligents car les portefeuilles avec le standard EOA participent automatiquement.

{% hint style="info" %}
Les contrats à signatures multiples ou les autres contrats intelligents doivent appeler la fonction `rebaseOptIn()` afin de générer du rendement.
{% endhint %}

Un des enjeux du rebasement d'une devise comme OUSD est que cela ne fonctionne pas très bien avec des teneurs de marché automatisé comme Uniswap ou Balancer. Ces marchés décentralisés reposent sur l'offre et la demande pour déterminer le prix de transaction d'un actifs. Cela amène des enjeux au niveau des calculs lorsque le nombre d'OUSD détenu dans un contrat est soudainement modifié en raison du rendement généré.

We previously added a [bandaid](https://medium.com/originprotocol/upgrades-to-the-ousd-smart-contracts-deliver-higher-yield-and-better-uniswap-support-aa592e51d3f2) that called Uniswap’s `sync()` function every time a `rebase()` was triggered on OUSD’s contracts. While this prevented users from seeing an ugly error message when they tried to trade OUSD on Uniswap, it still introduced loss into the system. After calling sync, Uniswap detects that there is more OUSD than USDT in the vault, which incorrectly pushes down the price of OUSD relative to USDT. While we can count on arbitrageurs to correct the price, it’s better if we can avoid this loss altogether. Given the ever-growing number of competitive AMM’s and forks of Uniswap, it would quickly become infeasible, not to mention gas-expensive, to try and special-case all of them.

After much discussion, we decided that the most scalable solution was to make smart contracts explicitly opt-in to receiving yield via the rebasing mechanism. This fixes the issue with the expanding supply on AMM’s while still allowing multi-sig wallets and other smart contracts the opportunity to still participate and earn yield.

{% hint style="warning" %}
If you are deploying a contract and intend to call`rebaseOptIn()`to earn yield you cannot call it from the contracts constructor. The contract must be deployed before it can be called.
{% endhint %}

If you are using a multi-sig wallet like [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) or [Gnosis Safe](https://gnosis-safe.io/), you will need the  [proxy contract address for OUSD](../../smart-contracts/registry.md) and the corresponding [ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805). Once you add those, you will be able to call the `rebaseOptIn()` function to opt into receiving yield via rebasing or`rebaseOptOut()` to turn it off again.





