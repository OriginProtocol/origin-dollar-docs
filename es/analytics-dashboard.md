# Panel de Análisis

{% hint style="info" %}
Visite [analytics.ousd.com](https://analytics.ousd.com) para ver cómo se asignan los fondos, ver los datos históricos de rendimiento y realizar un seguimiento de sus ganancias personales.
{% endhint %}

El [Panel APY](https://analytics.ousd.com/apy) está destinado principalmente para el consumo de nuestro equipo de ingeniería, pero seguimos adelante y lo implementamos ya que nuestro espíritu es "público por defecto" y todo lo que hacemos es [de código abierto](http://github.com/OriginProtocol). Desafortunadamente, eso a menudo significa equivocarse por el lado de la transparencia y no necesariamente por tomarse el tiempo para explicar las cosas con claridad.

Antes de sumergirse en el cálculo del rendimiento, es importante comprender cómo funciona OUSD tanto en términos de [generación de rendimiento](https://docs.ousd.com/core-concepts/yield-generation) como de [rebase](https://docs.ousd.com/core-concepts/elastic-supply). You can read all about that in these [docs](https://docs.ousd.com), including [the part about smart contracts being excluded from yield](https://docs.ousd.com/core-concepts/elastic-supply/rebasing-and-smart-contracts).

Para resumir cómo se calcula el APY, es la tasa de cambio anualizada en la contabilidad interna de OUSD de los saldos de los usuarios entre dos puntos en el tiempo. To understand that, let's break down the columns in the historical APY table (in reverse order).

**Proporción**

There are two types of OUSD balances: rebasing (most accounts) and non-rebasing (smart contracts that have not opted in). El contrato del token OUSD mantiene una contabilidad interna separada para cada tipo de saldo usando lo que llama "créditos". La relación que se muestra aquí es la oferta de rebase de OUSD dividida por los créditos de rebase, lo que nos da el tipo de cambio entre los dos.

**Créditos**

Some smart contracts holding OUSD have unique credit balances because their rebasing status has changed at some point in the past (by opting in or out). Aquí mostramos la suma de todos los créditos de rebase y créditos sin rebase. Cuando se multiplica por la relación, da la diferencia entre la oferta de respaldo y la oferta sin rebase.

**Sin rebase**

Esta es la parte del suministro que se encuentra en otros contratos inteligentes que no han optado por el rebase. When added to (credits \* ratio), this equals backing supply. Tenga en cuenta también que el **%** muestra el porcentaje de OUSD que no es realiza rebase.

**Aumentar**

El APY se "aumenta" efectivamente para las cuentas de rebase gracias al hecho de que algunos OUSD no realizan rebase. Piense en todas las monedas estables que se utilizaron como garantía para acuñar OUSD sin rebase. Esas monedas estables siguen obteniendo ganancias a través de nuestras estrategias de farming de rendimiento, pero las ganancias se acumulan solo en las cuentas de rebase. El resultado es que el APY efectivo es más alto de lo que sería sin este mecanismo. El aumento es la medida de esta diferencia. Si el aumento es del 100%, los titulares regulares de OUSD disfrutan del doble de APY que de otra manera.

**Cálculo APR/APY**

Llevando este círculo completo, actualmente medimos el rendimiento midiendo el cambio en los [créditos de rebase por token](https://github.com/OriginProtocol/origin-dollar/blob/master/contracts/contracts/token/OUSD.sol#L45) entre dos puntos en el tiempo. Pero hay algunas otras consideraciones a tener en cuenta. Primero, debemos suponer cuántos bloques de Ethereum se minan en un día promedio. Usamos un [fijo de 6.500](https://github.com/OriginProtocol/ousd-analytics/blob/master/eagleproject/core/views.py#L43), pero el número real de bloques por día es variable. En segundo lugar, necesitamos un horizonte temporal razonable para medir. Nos centramos en [7 días](https://github.com/OriginProtocol/ousd-analytics/blob/master/eagleproject/core/views.py#L422), que ha demostrado ser una ventana de tiempo relativamente constante durante la cual se ha producido una muestra completa de actividades generadoras de rendimiento. En tercer lugar, convertimos el APR en APY asumiendo una [composición diaria constante](https://github.com/OriginProtocol/ousd-analytics/blob/master/eagleproject/core/views.py#L449-L451). En otras palabras, el rendimiento se reinvierte constantemente en las mismas estrategias. Por último, hay un inconveniente notable en el uso de la relación de rebase para medir el rendimiento. Since rebase events currently occur sporadically (and not very frequently in a world of high gas prices), the APY won't reflect earnings that have not yet been translated to account balances. Por ejemplo, podría haber un aumento en la tasa de interés en Compound o un aumento en el volumen en la estrategia Curve 3pool, lo que haría que OUSD ganara más de lo que gana en un día promedio. Hasta que [el método de rebase](https://github.com/OriginProtocol/origin-dollar/blob/master/contracts/contracts/vault/VaultCore.sol#L365-L370) es llamado, el APY subreporta estas ganancias. In fact, anyone who sells OUSD during that time would be missing out on the "[next rebase](https://analytics.ousd.com)". The good news is that you should be able to observe the change in your balance over one week and it (annualized) should approximately equal our advertised APY.
