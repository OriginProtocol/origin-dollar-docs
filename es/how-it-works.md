# Cómo funciona

#### 100% Respaldado y Estable

Origin Dollar \ (OUSD \) es un token compatible con ERC-20 para la red de Ethereum.

OUSD es una moneda estable que está respaldada 1:1 por otras monedas estables como USDT, USDC y DAI. Como resultado, 1 OUSD siempre debería estar muy cerca de 1 USD en valor.

{% hint style="success" %}
1 OUSD = 1 USD
{% endhint %}

#### Acuñar OUSD

Los usuarios convierten sus monedas estables existentes \ (actualmente USDT, USDC y DAI \) a OUSD en el [Origin Dollar DApp](www.ousd.com)oficial. El OUSD emitido comienza a acumular rendimiento compuesto de inmediato.

**Canjeando OUSD**

Los usuarios pueden volver a convertir su OUSD en otras monedas estables en cualquier momento utilizando [Origin Dollar DApp](www.ousd.com). A 0.5% exit fee is charged upon redemption and is distributed as additional yield to the remaining participants in the vault. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from syphoning stablecoins from the vault in the event of mispricings of of the underlying assets. La tarifa existe para incentivar a los holders a largo plazo sobre los especuladores a corto plazo.

Tras el canje, el contrato inteligente determinará qué moneda estable \ (s \) devolver al usuario. In the current implementation, the vault will return coins in the same ratio as the current holdings. This lack of user optionality also protects the vault as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}
Hay una tarifa de salida de **0.5%** y el usuario no puede elegir qué monedas estables recibe.
{% endhint %}

#### **Rendimiento de Cultivo Automatizado **

OUSD genera rendimientos mediante la implementación de las monedas estables subyacentes que se depositaron en el contrato inteligente de OUSD en otros protocolos DeFi como Compound, Aave, Uniswap, Balancer y Curve. It is expected there will be new diversified strategies added to the vault every month. Los intereses cobrados, las tarifas de tradeo y los tokens de recompensa se agrupan y se convierten en monedas estables para producir rendimientos denominados en OUSD. Con el tiempo, el protocolo moverá activos dentro y fuera de diferentes grupos de liquidez para brindar el mejor rendimiento a los holders de OUSD.

#### **Suministro Elástico**

Los rendimientos generados se transmiten a los holders de OUSD a través de un constante rebase de la oferta monetaria. OUSD ajusta constantemente la oferta monetaria en respuesta al rendimiento que ha generado el protocolo. Esto permite que el precio de OUSD se mantenga fijo en $1 USD mientras que los saldos en las billeteras de los holders de tokens se ajustan en tiempo real para reflejar los rendimientos que se han obtenido mediante el protocolo.

El resultado final es una moneda estable que es fácil de gastar, obtiene rendimientos enormes automáticamente y es más deseable de mantener que las monedas estables existentes.

