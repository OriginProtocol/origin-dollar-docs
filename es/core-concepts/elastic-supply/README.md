# Suministro Elástico

**Suministro Elástico. Precio estable.**

OUSD funciona de manera diferente a la mayoría de los tokens. Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. En cambio, los contratos ajustan constantemente el suministro monetario y actualizan automáticamente el saldo en la billetera de cada holder de tokens para reflejar el rendimiento obtenido por el protocolo.

{% hint style="info" %}
Piense en ello como intereses acumulados en su cuenta bancaria. La unidad de cuenta y el valor del dólar estadounidense no cambian. Simplemente obtiene más dólares estadounidenses a medida que gana intereses.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD está respaldado al 100% por otras monedas estables y no tiene el mismo desafío de mantener la paridad con el dólar. Dada la facilidad de acuñar y canjear OUSD, podemos contar con arbitrajistas para garantizar que se mantenga la paridad.
2. El rebasamiento de OUSD está fuertemente sesgado hacia el aumento de la oferta, ya que la cantidad de OUSD acuñada está vinculada a las ganancias obtenidas por las estrategias subyacentes. Su principal está protegido siempre que nada salga mal con los protocolos subyacentes de préstamos/AMM y moneda estable. Su saldo de OUSD nunca disminuirá, pero el valor podría disminuir si hay una falla en los sistemas subyacentes.
3. A diferencia de Ampleforth, que se reactiva una vez al día, la oferta monetaria de OUSD se actualiza constantemente en tiempo real a medida que se genera el rendimiento. Las nuevas bases se activan regularmente a medida que los usuarios interactúan con los contratos de OUSD.

**Activación manual de una rebase**

Cualquiera puede activar una rebase en cualquier momento [llamando a la función de rebase en la bóveda](https://etherscan.io/address/originvault.eth#writeProxyContract). Puede hacer esto en Etherscan conectando una billetera web3.
