# Ribasamento & Smart Contract

Se stai utilizzando un wallet multi-sig o un altro smart contract che intende sincronizzarsi con i rebasamenti di OUSD, devi richiamare la funzione `rebaseOptIn()` dello smart contract di OUSD. Questo si deve fare solo con gli smart contract perché i wallet EOA vengono registrati automaticamente.

{% hint style="info" %}
I wallet multi-sig o altri smart contract devono richiamare la funzione ` rebaseOptIn()` per cominciare ad accumulare rendimento.
{% endhint %}

By default, OUSD that is held on smart contracts will not participate in the rebasing nature of the token and will forfeit any yield unless the smart contract explicitly opts-in. This increases the composability of OUSD within DeFi as many protocols weren't designed with the expectation that balances might change. To other DeFi protocols, OUSD works just like any other normal, well-behaved ERC-20 until you ask it to change. This is a particularly useful attribute for automated market makers (AMM’s) like Uniswap which break when the number of tokens they are holding changes unexpectedly.

![The Gnosis Safe OUSD app will prompt you to opt in to yield](../../.gitbook/assets/ousd-app-in-gnosis-safe.png)

Smart contracts must explicitly opt-in to receiving yield via the rebasing mechanism. This fixes the issue with the expanding supply on AMM’s while still allowing multi-sig wallets and other smart contracts the opportunity to still participate and earn yield.

{% hint style="warning" %}
If you are deploying a contract and intend to call`rebaseOptIn()`to earn yield you cannot call it from the contract's constructor. The contract must be deployed before it can be called.
{% endhint %}

[Gnosis Safe](https://gnosis-safe.io) users are encouraged to use the Origin Dollar app which will prompt you to opt in to receiving yield. If you are using the "Old" [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) or another contract-based wallet, you will need the [proxy contract address for OUSD](../../smart-contracts/registry.md) and the corresponding [ABI](https://api.etherscan.io/api?module=contract\&action=getabi\&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805). Once you add those, you will be able to call the `rebaseOptIn()` function to opt into receiving yield via rebasing or`rebaseOptOut()` to turn it off again.



