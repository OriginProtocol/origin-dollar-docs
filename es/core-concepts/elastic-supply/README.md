# Suministro Elástico

**Suministro Elástico. Precio estable.**

OUSD funciona de manera diferente a la mayoría de los tokens. En lugar de que el precio aumente a medida que aumenta el valor de los activos bajo administración \ (como con los cTokens de Compound o los yTokens de Yearn \), el valor de un OUSD permanece constante en aproximadamente $1. En cambio, los contratos ajustan constantemente el suministro monetario y actualizan automáticamente el saldo en la billetera de cada holder de tokens para reflejar el rendimiento obtenido por el protocolo.

{% hint style="info" %}
Piense en ello como intereses acumulados en su cuenta bancaria. La unidad de cuenta y el valor del dólar estadounidense no cambian. Simplemente obtiene más dólares estadounidenses a medida que gana intereses.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

Este mecanismo se inspiró en el enfoque novedoso adoptado por [Ampleforth](https://www.ampleforth.org/), pero hay algunas diferencias clave que vale la pena destacar:

1. OUSD is 100% backed by other stablecoins and does not have the same challenge maintaining the peg to the dollar. Dada la facilidad de acuñar y canjear OUSD, podemos contar con arbitrajistas para garantizar que se mantenga la paridad.
2. OUSD rebasing will only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Your OUSD balance will never decrease, but the value could drop if there's a failure in the underlying systems.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebases are triggered regularly as users interact with the OUSD contracts.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.

