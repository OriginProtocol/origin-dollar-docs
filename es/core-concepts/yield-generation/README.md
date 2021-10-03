# Generación de rendimiento

**Cultivo de Rendimiento Automatizado**

Si bien la explosión Cámbrica de nuevos préstamos y grupos de creadores de mercado automatizados ha impulsado el valor total bloqueado \(TVL\), también ha hecho que sea cada vez más difícil para los cultivadores de rendimiento asignar capital manualmente de manera eficiente y óptima.

[Yearn](https://yearn.finance/) ha demostrado que los contratos inteligentes pueden automatizar el reequilibrio de fondos en varias estrategias para ganar de manera óptima intereses de préstamos, tarifas de creación de mercado y tokens de recompensa. Con el tiempo, se implementarán nuevas estrategias que maximizan los retornos y minimizan el riesgo y las dependencias.

![Recolección de rendimiento automatizada en el protocolo OUSD](../../.gitbook/assets/ousd_earnings_graphic.png)

OUSD utiliza las siguientes estrategias de alto nivel para generar rendimiento:

{% page-ref page="lending.md" %}

{% page-ref page="market-making.md" %}

{% page-ref page="rewards.md" %}

OUSD puede generar mayores rendimientos que los protocolos de la competencia debido a una combinación de importantes decisiones de diseño que amplifican las recompensas que se devuelven a los holders de OUSD:

* Las tarifas de salida se devuelven al grupo de liquidez, recompensando a los holders a largo plazo
* Los oráculos de precios favorecen al colectivo sobre el individual, recompensando nuevamente a los holders a largo plazo
* Los contratos inteligentes deben optar manualmente para obtener rendimiento. Esto permite que el protocolo ponga más capital a trabajar de lo que sería posible de otra manera.
* Las estrategias inteligentes equilibran el riesgo y la recompensa de manera más eficaz que la implementación de capital en una sola estrategia subyacente.

