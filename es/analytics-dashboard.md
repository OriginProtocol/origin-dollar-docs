# Panel de Análisis

{% hint style="info" %}
Visite [analytics.ousd.com](https://analytics.ousd.com) para ver cómo se asignan los fondos, ver los datos históricos de rendimiento y realizar un seguimiento de sus ganancias personales.
{% endhint %}

El [Panel APY](https://analytics.ousd.com/apy) está destinado principalmente para el consumo de nuestro equipo de ingeniería, pero seguimos adelante y lo implementamos ya que nuestro espíritu es "público por defecto" y todo lo que hacemos es [de código abierto](http://github.com/OriginProtocol). Desafortunadamente, eso a menudo significa equivocarse por el lado de la transparencia y no necesariamente por tomarse el tiempo para explicar las cosas con claridad.

Antes de sumergirse en el cálculo del rendimiento, es importante comprender cómo funciona OUSD tanto en términos de [generación de rendimiento](https://docs.ousd.com/core-concepts/yield-generation) como de [rebase](https://docs.ousd.com/core-concepts/elastic-supply). Puede leer todo sobre eso en estos [documentos](https://docs.ousd.com), incluyendo [sobre los contratos inteligentes que se excluyen del rendimiento](https://docs.ousd.com/core-concepts/elastic-supply/rebasing-and-smart-contracts).

Para resumir cómo se calcula el APY, es la tasa de cambio anualizada en la contabilidad interna de OUSD de los saldos de los usuarios entre dos puntos en el tiempo. Para entender eso, analicemos las columnas de la tabla APY histórica (en orden inverso).

**Proporción**

Hay dos tipos de saldos de OUSD: rebasing (la mayoría de las cuentas) y no rebasing (contratos inteligentes que no han optado por participar). El contrato del token OUSD mantiene una contabilidad interna separada para cada tipo de saldo usando lo que llama "créditos". La relación que se muestra aquí es la oferta de rebase de OUSD dividida por los créditos de rebase, lo que nos da el tipo de cambio entre los dos.

**Créditos**

Algunos contratos inteligentes que tienen OUSD tienen saldos de crédito únicos porque su estado de rebase ha cambiado en algún momento en el pasado (al optar por participar o no). Aquí mostramos la suma de todos los créditos de rebase y créditos sin rebase. Cuando se multiplica por la relación, da la diferencia entre la oferta de respaldo y la oferta sin rebase.

**Sin rebase**

Esta es la parte del suministro que se encuentra en otros contratos inteligentes que no han optado por el rebase. Cuando se suma a (proporción de créditos \*), esto equivale al suministro de respaldo. Tenga en cuenta también que el **%** muestra el porcentaje de OUSD que no es realiza rebase.

**Aumentar**

El APY se "aumenta" efectivamente para las cuentas de rebase gracias al hecho de que algunos OUSD no realizan rebase. Piense en todas las monedas estables que se utilizaron como garantía para acuñar OUSD sin rebase. Esas monedas estables siguen obteniendo ganancias a través de nuestras estrategias de farming de rendimiento, pero las ganancias se acumulan solo en las cuentas de rebase. El resultado es que el APY efectivo es más alto de lo que sería sin este mecanismo. El aumento es la medida de esta diferencia. Si el aumento es del 100%, los titulares regulares de OUSD disfrutan del doble de APY que de otra manera.

**Cálculo APR/APY**

Bringing this full circle, we currently measure yield by measuring the change in the [rebasing credits per token](https://github.com/OriginProtocol/origin-dollar/blob/master/contracts/contracts/token/OUSD.sol#L45) between two points in time. Pero hay algunas otras consideraciones a tener en cuenta. Primero, debemos suponer cuántos bloques de Ethereum se minan en un día promedio. Usamos un [fijo de 6.500](https://github.com/OriginProtocol/ousd-analytics/blob/master/eagleproject/core/views.py#L43), pero el número real de bloques por día es variable. En segundo lugar, necesitamos un horizonte temporal razonable para medir. We focus on 30 days, which has proven to be a relatively consistent window of time during which a complete sample of yield-generating activities has occurred. En tercer lugar, convertimos el APR en APY asumiendo una [composición diaria constante](https://github.com/OriginProtocol/ousd-analytics/blob/master/eagleproject/core/views.py#L449-L451). En otras palabras, el rendimiento se reinvierte constantemente en las mismas estrategias. Por último, hay un inconveniente notable en el uso de la relación de rebase para medir el rendimiento. Dado que los eventos de rebase actualmente ocurren esporádicamente (y no con mucha frecuencia en un mundo de altos precios de gas), el APY no reflejará las ganancias que aún no se hayan traducido a saldos de cuenta. Por ejemplo, podría haber un aumento en la tasa de interés en Compound o un aumento en el volumen en la estrategia Curve 3pool, lo que haría que OUSD ganara más de lo que gana en un día promedio. Hasta que [el método de rebase](https://github.com/OriginProtocol/origin-dollar/blob/master/contracts/contracts/vault/VaultCore.sol#L365-L370) es llamado, el APY subreporta estas ganancias. De hecho, cualquiera que venda OUSD durante ese tiempo se estaría perdiendo el "[siguiente rebase](https://analytics.ousd.com)". La buena noticia es que debería poder observar el cambio en su saldo durante una semana y (anualizado) debería ser aproximadamente igual a nuestro APY anunciado.
