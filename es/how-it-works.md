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

Los usuarios pueden volver a convertir su OUSD en otras monedas estables en cualquier momento utilizando [Origin Dollar DApp](www.ousd.com). Se cobra una tarifa de salida del 0,5% en el momento del canje y se distribuye como rendimiento adicional a los participantes restantes en el grupo de liquidez. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from siphoning stablecoins from the vault in the event of mispriced underlying assets. La tarifa existe para incentivar a los holders a largo plazo sobre los especuladores a corto plazo.

Tras el canje, el contrato inteligente determinará qué moneda estable \ (s \) devolver al usuario. En la implementación actual, el grupo de liquidez devolverá monedas en la misma proporción que las existencias actuales. Esta falta de opciones para el usuario también protege al grupo de liquidez en su conjunto en caso de que alguna de las monedas estables admitidas pierda su vínculo con el dólar.

{% hint style="warning" %}
Hay una tarifa de salida de **0.5%** y el usuario no puede elegir qué monedas estables recibe.
{% endhint %}

#### **Rendimiento de Cultivo Automatizado **

OUSD generates yields by deploying the underlying stablecoins that were deposited to the OUSD smart contract to other DeFi protocols such as Compound, Aave, and Curve. There may be new diversified strategies added to the vault in the future. Los intereses cobrados, las tarifas de tradeo y los tokens de recompensa se agrupan y se convierten en monedas estables para producir rendimientos denominados en OUSD. Con el tiempo, el protocolo moverá activos dentro y fuera de diferentes grupos de liquidez para brindar el mejor rendimiento a los holders de OUSD.

#### **Suministro Elástico**

Los rendimientos generados se transmiten a los holders de OUSD a través de un constante rebase de la oferta monetaria. OUSD ajusta constantemente la oferta monetaria en respuesta al rendimiento que ha generado el protocolo. Esto permite que el precio de OUSD se mantenga fijo en $1 USD mientras que los saldos en las billeteras de los holders de tokens se ajustan en tiempo real para reflejar los rendimientos que se han obtenido mediante el protocolo.

El resultado final es una moneda estable que es fácil de gastar, obtiene rendimientos enormes automáticamente y es más deseable de mantener que las monedas estables existentes.

