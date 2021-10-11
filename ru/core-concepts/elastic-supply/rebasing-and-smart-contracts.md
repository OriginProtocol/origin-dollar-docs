# Перераспределение & Смарт-Контракты

Если Вы используете кошелек с мульти-подписями или другой смарт-контракт для участия в перераспределении OUSD, Вы должны вызвать функцию OUSD `rebaseOptIn()`. Это относится только к смарт-контрактам, так как стандартные кошельки EOA регистрируются автоматически.

{% hint style="info" %}
Кошельки с мульти-подписями или другие смарт-контракты должны вызвать функцию `rebaseOptIn()` чтобы получать доход.
{% endhint %}

По умолчанию, OUSD на смарт-контрактах не будет участвовать в перераспределении токена и потеряет любой доход, если смарт-контракт явным образом не поддерживает функцию получения токенов. Это увеличивает уровень "сочетаемости" OUSD с DeFi, поскольку многие протоколы не были разработаны с расчетом на изменение баланса. Для других протоколов DeFi OUSD работает так же, как и любой другой нормальный токен протокола ERC-20. This is a particularly useful attribute for automated market makers (AMM’s) like Uniswap which break when the number of tokens they are holding changes unexpectedly.

![The Gnosis Safe OUSD app will prompt you to opt in to yield](../../.gitbook/assets/ousd-app-in-gnosis-safe.png)

Smart contracts must explicitly opt-in to receiving yield via the rebasing mechanism. This fixes the issue with the expanding supply on AMM’s while still allowing multi-sig wallets and other smart contracts the opportunity to still participate and earn yield.

{% hint style="warning" %}
If you are deploying a contract and intend to call`rebaseOptIn()`to earn yield you cannot call it from the contract's constructor. The contract must be deployed before it can be called.
{% endhint %}

[Gnosis Safe](https://gnosis-safe.io) users are encouraged to use the Origin Dollar app which will prompt you to opt in to receiving yield. If you are using the "Old" [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) or another contract-based wallet, you will need the [proxy contract address for OUSD](../../smart-contracts/registry.md) and the corresponding [ABI](https://api.etherscan.io/api?module=contract\&action=getabi\&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805). Once you add those, you will be able to call the `rebaseOptIn()` function to opt into receiving yield via rebasing or`rebaseOptOut()` to turn it off again.



