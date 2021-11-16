# Suministro Elástico

**Suministro Elástico. Precio estable.**

OUSD funciona de manera diferente a la mayoría de los tokens. Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. Instead, the contracts constantly adjust the monetary supply and automatically updates the balance in every token holder’s wallet to reflect the yield that has been earned by the protocol.&#x20;

{% hint style="info" %}
Piense en ello como intereses acumulados en su cuenta bancaria. La unidad de cuenta y el valor del dólar estadounidense no cambian. Simplemente obtiene más dólares estadounidenses a medida que gana intereses.
{% endhint %}

![](../../.gitbook/assets/ousd\_docs\_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD está respaldado al 100% por otras monedas estables y no tiene el mismo desafío de mantener la paridad con el dólar. Given the ease of minting and redeeming OUSD, we can count on arbitrageurs to ensure the peg is maintained.&#x20;
2. El rebasamiento de OUSD está fuertemente sesgado hacia el aumento de la oferta, ya que la cantidad de OUSD acuñada está vinculada a las ganancias obtenidas por las estrategias subyacentes. Su principal está protegido siempre que nada salga mal con los protocolos subyacentes de préstamos/AMM y moneda estable. Su saldo de OUSD nunca disminuirá, pero el valor podría disminuir si hay una falla en los sistemas subyacentes.
3. Unlike Ampleforth, which only rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Las nuevas bases se activan regularmente a medida que los usuarios interactúan con los contratos de OUSD. Chainlink Keepers ensure at least one rebase occurs every day.

**Activación manual de una rebase**

Cualquiera puede activar una rebase en cualquier momento [llamando a la función de rebase en la bóveda](https://etherscan.io/address/originvault.eth#writeProxyContract). Puede hacer esto en Etherscan conectando una billetera web3.
