# Suministro Elástico

**Suministro Elástico. Precio estable.**

OUSD funciona de manera diferente a la mayoría de los tokens. En lugar de que el precio aumente a medida que aumenta el valor de los activos bajo administración \ (como con los cTokens de Compound o los yTokens de Yearn \), el valor de un OUSD permanece constante en aproximadamente $1. En cambio, los contratos ajustan constantemente el suministro monetario y actualizan automáticamente el saldo en la billetera de cada holder de tokens para reflejar el rendimiento obtenido por el protocolo.

{% hint style="info" %}
Piense en ello como intereses acumulados en su cuenta bancaria. La unidad de cuenta y el valor del dólar estadounidense no cambian. Simplemente obtiene más dólares estadounidenses a medida que gana intereses.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

Este mecanismo se inspiró en el enfoque novedoso adoptado por [Ampleforth](https://www.ampleforth.org/), pero hay algunas diferencias clave que vale la pena destacar:

1. OUSD está respaldado al 100% por otras monedas estables y no tiene el mismo desafío de mantener la paridad con el dólar. Dada la facilidad de acuñar y canjear OUSD, podemos contar con arbitrajistas para garantizar que se mantenga la paridad.
2. El rebasamiento de OUSD está fuertemente sesgado hacia el aumento de la oferta, ya que la cantidad de OUSD acuñada está vinculada a las ganancias obtenidas por las estrategias subyacentes. Su principal está protegido siempre que nada salga mal con los protocolos subyacentes de préstamos/AMM y moneda estable. Su saldo de OUSD nunca disminuirá, pero el valor podría disminuir si hay una falla en los sistemas subyacentes.
3. A diferencia de Ampleforth, que se reactiva una vez al día, la oferta monetaria de OUSD se actualiza constantemente en tiempo real a medida que se genera el rendimiento. Rebases are triggered regularly as users interact with the OUSD contracts.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.

