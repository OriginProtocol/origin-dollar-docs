# Suministro Elástico

**Suministro Elástico. Precio estable.**

OUSD funciona de manera diferente a la mayoría de los tokens. En lugar de que el precio aumente a medida que aumenta el valor de los activos bajo administración (como con Compound cTokens o Yearn yTokens), el valor de un OUSD permanece constante en aproximadamente $1. En cambio, los contratos ajustan constantemente el suministro monetario y actualizan automáticamente el saldo en la billetera de cada holder de tokens para reflejar el rendimiento que ha obtenido el protocolo.&#x20;

{% hint style="info" %}
Piense en ello como intereses acumulados en su cuenta bancaria. La unidad de cuenta y el valor del dólar estadounidense no cambian. Simplemente obtiene más dólares estadounidenses a medida que gana intereses.
{% endhint %}

![](../../.gitbook/assets/ousd\_docs\_graphics\_4.png)

Este mecanismo se inspiró en el enfoque novedoso adoptado por [Ampleforth](https://www.ampleforth.org), pero hay algunas diferencias clave que vale la pena destacar:

1. OUSD está respaldado al 100% por otras monedas estables y no tiene el mismo desafío de mantener la paridad con el dólar. Dada la facilidad de acuñar y canjear OUSD, podemos contar con arbitrajistas para garantizar que se mantenga la paridad.&#x20;
2. El rebasamiento de OUSD está fuertemente sesgado hacia el aumento de la oferta, ya que la cantidad de OUSD acuñada está vinculada a las ganancias obtenidas por las estrategias subyacentes. Su principal está protegido siempre que nada salga mal con los protocolos subyacentes de préstamos/AMM y moneda estable. Su saldo de OUSD nunca disminuirá, pero el valor podría disminuir si hay una falla en los sistemas subyacentes.
3. A diferencia de Ampleforth, que solo se realiza rebase una vez al día, la oferta monetaria de OUSD se actualiza constantemente en tiempo real a medida que se genera el rendimiento. Las nuevas bases se activan regularmente a medida que los usuarios interactúan con los contratos de OUSD. Chainlink Keepers se asegura de que se produzca al menos un rebase todos los días.

**Activación manual de una rebase**

Cualquiera puede activar una rebase en cualquier momento [llamando a la función de rebase en la bóveda](https://etherscan.io/address/originvault.eth#writeProxyContract). Puede hacer esto en Etherscan conectando una billetera web3.
