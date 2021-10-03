# Rebase & Contratos Inteligentes

Si está utilizando una billetera multi-sig u otro contrato inteligente que desea participar en el aspecto de rebase de OUSD, debe llamar a la función `rebaseOptIn()` de OUSD. Esto solo se aplica a los contratos inteligentes, ya que las billeteras EOA estándar se inscriben automáticamente.

{% hint style="info" %}
Las billeteras multi-sig u otros contratos inteligentes deben llamar a `rebaseOptIn()` para obtener rendimiento.
{% endhint %}

De forma predeterminada, el OUSD que se mantiene en contratos inteligentes no participará en la naturaleza de rebase del token y perderá cualquier rendimiento a menos que el contrato inteligente lo acepte explícitamente. Esto aumenta la capacidad de composición de OUSD dentro de DeFi, ya que muchos protocolos no se diseñaron con la expectativa de que los equilibrios pudieran cambiar. Para otros protocolos DeFi, OUSD funciona como cualquier otro ERC-20 normal y de buen comportamiento hasta que le pida que cambie. Este es un atributo particularmente útil para los creadores de mercado automatizados \(AMMs\) como Uniswap, que se rompen cuando la cantidad de tokens que tienen cambia inesperadamente.

![La aplicación Gnosis Safe de OUSD le pedirá que opte por ceder](../../.gitbook/assets/ousd-app-in-gnosis-safe.png)

Los contratos inteligentes deben optar explícitamente por recibir rendimiento a través del mecanismo de reajuste. Esto soluciona el problema con la oferta en expansión de AMM y, al mismo tiempo, permite que las billeteras multi-sig y otros contratos inteligentes tengan la oportunidad de participar y obtener rendimiento.

{% hint style="warning" %}
Si está implementando un contrato y tiene la intención de llamar a`rebaseOptIn()`para obtener rendimiento, no puede llamarlo desde el constructor del contrato. El contrato debe implementarse antes de que se pueda llamar.
{% endhint %}

[Se recomienda a los usuarios de Gnosis Safe](https://gnosis-safe.io/) que utilicen la aplicación Origin Dollar, que le pedirá que opte por recibir rendimiento. Si está utilizando la "Antigua" [Gnosis Wallet](https://github.com/gnosis/MultiSigWallet) u otra billetera basada en contrato, necesitará [la dirección de contrato para OUSD](../../smart-contracts/registry.md) y el correspondiente [ABI](https://api.etherscan.io/api?module=contract&action=getabi&address=0x1ae95dd4eeae7ed03da79856c2d44ffa3318f805). Una vez que los agregue, podrá llamar a la función `rebaseOptIn()` para optar por recibir rendimiento a través de rebase o`rebaseOptOut()` para apagarlo nuevamente.





