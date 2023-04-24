# Empezando

Estos documentos están destinados a explicar cómo funciona OUSD, comunicar los riesgos y beneficios potenciales y proporcionar una guía para los desarrolladores que deseen contribuir a nuestro código base o integrar OUSD en sus productos. Aquí hay algunas formas en las que puede sumergirse y comenzar.

**Comprando OUSD**

{% hint style="info" %}
La [DApp de Origin Dollar](https://ousd.com/swap) enrutará inteligentemente su transacción para obtener la mejor tarifa.
{% endhint %}

La [DApp de Origin Dollar](https://ousd.com/swap) permite a cualquier persona comprar o vender OUSD utilizando una billetera de criptomonedas compatible con web-3 como [Metamask](https://www.metamask.io), [Ledger](https://www.ledger.com) o [Gnosis Safe](https://gnosis-safe.io). Esta es la forma nativa de obtener OUSD, especialmente si desea una gran cantidad que podría arriesgar el movimiento del mercado en otros exchanges. La DApp decidirá inteligentemente si crear o intercambiar tokens OUSD utilizando la bóveda o lo ayudará a completar el intercambio en el AMM que actualmente ofrezca la mejor tarifa.

**Exchanges descentralizados**

OUSD está disponible actualmente en los siguientes exchanges descentralizados. Estos se enumeran aquí solo como referencia. Recomendamos utilizar la [DApp de Origin Dollar](https://ousd.com/swap) para asegurarse de obtener siempre la mejor tarifa.

* [Compre OUSD en 1inch](https://app.1inch.io/#/1/swap/USDT/OUSD)
* [Compre OUSD en Curve](https://curve.fi/factory/9)
* [Compre OUSD en Uniswap v3](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7\&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)
* [Compre OUSD en Uniswap v2](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7\&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86\&use=v2)
* [Compre OUSD en Sushiswap](https://exchange.sushiswapclassic.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7\&outputCurrency=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86)

**Exchanges centralizados**

OUSD está disponible actualmente en los siguientes exchanges centralizados. Asegúrese de verificar cómo manejan el rendimiento que genera el protocolo. Dependiendo del exchange, puede haber pasos adicionales que deba seguir para participar en el rendimiento mientras está bajo su custodia.

* Compre OUSD en KuCoin
  * [OUSD/USDT](https://trade.kucoin.com/OUSD-USDT)
  * [OUSD/BTC](https://trade.kucoin.com/OUSD-BTC)
* Buy OUSD on Gate.io
  * [OUSD/USDT](https://www.gate.io/trade/OUSD\_USDT)
* Buy OUSD on Virgox
  * [OUSD/USDT](https://virgox.com/exchange/141)
* [Buy OUSD on Dharma App](https://www.dharma.io) (US only)

Seguimos trabajando para que OUSD esté disponible en exchanges centralizados adicionales.

**Agregando OUSD a su billetera**

{% hint style="success" %}
La dirección ERC20 principal de Origin Dollar(OUSD) es: \
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

Si su OUSD no aparece automáticamente en su billetera, debería poder agregarlo manualmente usando la dirección anterior. Si usted está planeando en [almacenar su OUSD en una billetera de múltiples firmas](core-concepts/elastic-supply/rebasing-and-smart-contracts.md), asegúrese de optar para recibir el rendimiento. Queremos que OUSD sea compatible con tantas billeteras como sea posible y que se incluya en todas las diversas listas de tokens conocidos. Agradeceríamos enormemente cualquier ayuda que pueda ofrecer en esta área.&#x20;

**Integrando OUSD**

OUSD es un token ERC-20 no estándar que requiere un trabajo de integración personalizado para la mayoría de las aplicaciones que desean admitirlo. En particular, es importante que los desarrolladores comprendan cómo funciona nuestro suministro elástico, ya que esto puede causar fácilmente un comportamiento inesperado.

Si es un proveedor de billetera o un intercambio de criptomonedas que está interesado en respaldar OUSD, consulte las siguientes guías:&#x20;

{% content-ref url="core-concepts/elastic-supply/rebasing-and-smart-contracts.md" %}
[rebasing-and-smart-contracts.md](core-concepts/elastic-supply/rebasing-and-smart-contracts.md)
{% endcontent-ref %}

{% content-ref url="smart-contracts/architecture.md" %}
[architecture.md](smart-contracts/architecture.md)
{% endcontent-ref %}

{% content-ref url="smart-contracts/api/" %}
[api](smart-contracts/api/)
{% endcontent-ref %}

**Panel de Desarrolladores**

Nuestro panel de desarrolladores interno está disponible en [analytics.ousd.com](https://analytics.ousd.com). El panel muestra el suministro circulante actual, los activos bajo administración en la bóveda y las asignaciones actuales entre cada una de las monedas estables y estrategias.

**Obtener ayuda**

Únase a la sala de #engineering de Origin Dollar en el servidor de [Discord](https://www.originprotocol.com/discord) de Origin.  Nuestro equipo y los miembros de nuestra comunidad esperan poder ayudarlo a construir. Sus preguntas nos ayudan a mejorar, así que no dude en preguntar si no encuentra aquí lo que busca.
