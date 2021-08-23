# Rebase & Contratos Inteligentes

Si está utilizando una billetera multi-sig u otro contrato inteligente que desea participar en el aspecto de rebase de OUSD, debe llamar a la función `rebaseOptIn()` de OUSD. Esto solo se aplica a los contratos inteligentes, ya que las billeteras EOA estándar se inscriben automáticamente.

{% hint style="info" %}
Las billeteras multi-sig u otros contratos inteligentes deben llamar a `rebaseOptIn()` para obtener rendimiento.
{% endhint %}

De forma predeterminada, el OUSD que se mantiene en contratos inteligentes no participará en la naturaleza de rebase del token y perderá cualquier rendimiento a menos que el contrato inteligente lo acepte explícitamente. Esto aumenta la capacidad de composición de OUSD dentro de DeFi, ya que muchos protocolos no se diseñaron con la expectativa de que los equilibrios pudieran cambiar. Para otros protocolos DeFi, OUSD funciona como cualquier otro ERC-20 normal y de buen comportamiento hasta que le pida que cambie. Este es un atributo particularmente útil para los creadores de mercado automatizados \(AMMs\) como Uniswap, que se rompen cuando la cantidad de tokens que tienen cambia inesperadamente.

![The Gnosis Safe OUSD app will prompt you to opt in to yield](../../.gitbook/assets/ousd-app-in-gnosis-safe.png)

Smart contracts must explicitly opt-in to receiving yield via the rebasing mechanism. This fixes the issue with the expanding supply on AMM’s while still allowing multi-sig wallets and other smart contracts the opportunity to still participate and earn yield.

{% hint style="warning" %}
If you are deploying a contract and intend to call`rebaseOptIn()`to earn yield you cannot call it from the contract's constructor. The contract must be deployed before it can be called.
{% endhint %}

[Gnosis Safe](https://gnosis-safe.io/) users are encouraged to use the Origin Dollar app which will prompt you to opt in to receiving yield. If you are using the "Old" [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) or another contract-based wallet, you will need the [proxy contract address for OUSD](../../smart-contracts/registry.md) and the corresponding [ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805). Once you add those, you will be able to call the `rebaseOptIn()` function to opt into receiving yield via rebasing or`rebaseOptOut()` to turn it off again.





