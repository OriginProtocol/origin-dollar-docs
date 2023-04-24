# Cómo funciona

#### 100% Respaldado y Estable

Origin Dollar (OUSD) is an ERC-20 compliant token for the Ethereum network.&#x20;

OUSD es una moneda estable que está respaldada 1:1 por otras monedas estables como USDT, USDC y DAI. Como resultado, 1 OUSD siempre debería estar muy cerca de 1 USD en valor.

{% hint style="success" %}
1 OUSD = 1 USD&#x20;
{% endhint %}

#### Comprando OUSD

Los usuarios pueden convertir sus monedas estables existentes (actualmente USDT, USDC y DAI) a OUSD en la [DApp de Origin Dollar](https://www.ousd.com) oficial. Received OUSD begins accruing compounding yield immediately.&#x20;

Origin DApp enrutará de forma inteligente las transacciones de los usuarios para ofrecerles el mejor precio disponible, teniendo en cuenta el deslizamiento y los costos del gas. Esto significa que la DApp a veces alentará a los usuarios a comprar OUSD que ya está en circulación en lugar de acuñar OUSD nuevo de la bóveda. The OUSD DApp will choose from multiple sources of liquidity and will suggest the option that gives the user the best possible rate.&#x20;

**Vendiendo OUSD**

Los usuarios pueden volver a convertir su OUSD en otras monedas estables en cualquier momento utilizando la [DApp de Origin Dollar](https://www.ousd.com). La Dapp de Origin enrutará de manera inteligente las transacciones de los usuarios para brindarles el mejor precio disponible, teniendo en cuenta el deslizamiento, los costos del gas y la tarifa de salida de la bóveda. Esto significa que la DApp a menudo ayudará a los usuarios a vender su OUSD en un AMM en lugar de canjear OUSD en la bóveda e incurrir en la tarifa de salida del protocolo.

A 0.25% exit fee is charged upon redemption with the vault. Esta tarifa se distribuye como rendimiento adicional a los participantes restantes en la bóveda (es decir, otros holders de OUSD). La tarifa sirve como una característica de seguridad para dificultar que los atacantes aprovechen los oráculos rezagados, lo que les impide desviar monedas estables de la bóveda en caso de activos subyacentes con un precio incorrecto. La tarifa existe para incentivar a los holders a largo plazo sobre los especuladores a corto plazo.

Tras el canje, la bóveda determinará qué monedas estables devolver al usuario. En la implementación actual, la bóveda devolverá monedas en la misma proporción que las existencias actuales. Esta falta de opciones para el usuario también protege a la bóveda en su conjunto en caso de que alguna de las monedas estables admitidas pierda su vínculo con el dólar.

{% hint style="warning" %}
Redemptions on the OUSD vault incur a **0.25% exit fee** and the user doesn't get to pick which stablecoins they receive. Los usuarios a menudo pueden evitar esta tarifa vendiendo en un AMM en su lugar.
{% endhint %}

#### **Rendimiento de Cultivo Automatizado **

OUSD genera rendimientos mediante la implementación de las monedas estables subyacentes que se depositaron en el contrato inteligente de OUSD en otros protocolos DeFi como Compound, Aave y Curve. Es posible que se agreguen nuevas estrategias diversificadas a la bóveda en el futuro. Los intereses cobrados, las tarifas de trading y los tokens de recompensa se agrupan y se convierten en monedas estables para producir rendimientos denominados en OUSD. Over time, the protocol will move assets in and out of different liquidity pools in order to provide the best yield to the holders of OUSD.&#x20;

#### **Suministro Elástico**

Los rendimientos generados se transmiten a los holders de OUSD a través de un constante rebase del suministro de la moneda. OUSD ajusta constantemente el suministro en respuesta al rendimiento que ha generado el protocolo. Esto permite que el precio de OUSD se mantenga vinculado a $1 mientras que los saldos en las billeteras de los titulares de tokens se ajustan en tiempo real para reflejar los rendimientos que se han obtenido mediante el protocolo.

El resultado final es una moneda estable que es fácil de gastar, obtiene grandes rendimientos automáticamente y es más deseable de mantener que las monedas estables existentes.
