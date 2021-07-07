# Empezando

Estos documentos están destinados a explicar cómo funciona OUSD, comunicar los riesgos y beneficios potenciales y proporcionar una guía para los desarrolladores que deseen contribuir a nuestro código base o integrar OUSD en sus productos. Aquí hay algunas formas en las que puede sumergirse y comenzar.

**Acuñar o Canjear**

Acuñar OUSD permite a cualquier persona crear o intercambiar tokens OUSD utilizando nuestra [DApp](www.ousd.com) y una billetera

 de criptomonedas habilitada para web-3 como [ Metamask](https://www.metamask.io). Esta es la forma nativa de obtener OUSD, especialmente si desea una gran cantidad que podría correr el riesgo de mover el mercado en otras plataformas de intercambio.</p> 

**Comprar en Plataformas de Intercambio**

Para pequeñas cantidades, la forma más fácil de comenzar a ganar con OUSD es comprarlo en una plataforma de intercambio (exchange) descentralizado como Uniswap. Anticipamos que OUSD pronto estará disponible en muchos más exchanges descentralizados y centralizados. 

Exchanges descentralizados:

* [Buy OUSD on 1inch](https://app.1inch.io/#/1/swap/USDT/OUSD)
* [Buy OUSD on Uniswap v3](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)
* [Buy OUSD on Uniswap v2](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86&use=v2)
* [Buy OUSD on Sushiswap](https://exchange.sushiswapclassic.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86)

Exchanges centralizados:

* Compre OUSD en KuCoin 
    * [OUSD/USDT](https://trade.kucoin.com/OUSD-USDT)
  * [OUSD/BTC](https://trade.kucoin.com/OUSD-BTC)
* Compre OUSD en Virgox 
    * [OUSD/USDT](https://virgox.com/exchange/141)
* [Compre OUSD en la aplicación Dharma](https://www.dharma.io/) \(solo en EE.UU.\)

**Agregar OUSD a su billetera**

{% hint style="success" %}

La dirección ERC20 principal para Origin Dollar \(OUSD\) es:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86** 

{% endhint %}

Si su OUSD no aparece automáticamente en su billetera, debería poder agregarlo manualmente usando la dirección anterior. Si usted está planeando en [almacenar su OUSD en una carpeta de múltiples sig](core-concepts/elastic-supply/rebasing-and-smart-contracts.md), asegúrese de opt-in para recibir el rendimiento. Queremos que OUSD sea compatible con tantas carteras como sea posible y que se incluya en todas las diversas listas de tokens conocidos. Agradeceríamos enormemente cualquier ayuda que pueda ofrecer en esta área. 

**Integrando OUSD**

OUSD es un token ERC-20 no estándar que requiere un trabajo de integración personalizado para la mayoría de las aplicaciones que desean admitirlo. En particular, es importante que los desarrolladores comprendan cómo funciona nuestro suministro elástico, ya que esto puede causar fácilmente un comportamiento inesperado.

Si usted es un proveedor de billetera o una plataforma de intercambio cripto que está interesado en respaldar OUSD, consulte las siguientes guías: 

{% page-ref page="core-concepts/elastic-supply/rebasing-and-smart-contracts.md" %}

{% page-ref page="smart-contracts/architecture.md" %}

{% page-ref page="smart-contracts/api/" %}

**Análisis del Desarrollador**

Nuestro panel de desarrollo interno está disponible en [analytics.ousd.com](https://analytics.ousd.com). El tablero muestra el suministro circulante actual, los activos bajo administración en la bóveda y las asignaciones actuales entre cada una de las monedas estables y estrategias.

**Obtener ayuda**

Únase a la chat de ingeniería de Origin Dollar \#engineering en el servidor de Origin [en Discord](www.originprotocol.com/discord).  Nuestro equipo y los miembros de nuestra comunidad esperan poder ayudarlo a construir. Sus preguntas nos ayudan a mejorar, así que no dude en preguntar si no puede encontrar lo que busca aquí.

