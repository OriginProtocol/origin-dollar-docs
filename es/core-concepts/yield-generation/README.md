# Generación de rendimiento

**Cultivo de Rendimiento Automatizado**

Si bien la explosión Cámbrica de nuevos préstamos y grupos de creadores de mercado automatizados ha impulsado el valor total bloqueado \(TVL\), también ha hecho que sea cada vez más difícil para los cultivadores de rendimiento asignar capital manualmente de manera eficiente y óptima.

[Yearn](https://yearn.finance/) ha demostrado que los contratos inteligentes pueden automatizar el reequilibrio de fondos en diversas estrategias para ganar de manera óptima intereses crediticios, tarifas de creación de mercado y tokens de recompensa. Over time, new strategies will be deployed that maximize returns while minimizing risk and dependencies.

![](../../.gitbook/assets/ousd_docs_graphics_1.png)

OUSD uses the following high-level strategies for generating yield:

{% page-ref page="lending.md" %}

{% page-ref page="market-making.md" %}

{% page-ref page="rewards.md" %}

OUSD is able to generate higher yields than competing protocols due to a combination of important design decisions that amplify the rewards that are returned to OUSD holders:

* Exit fees are returned to the pool, rewarding long term holders
* Price oracles favor the collective over the individual, again rewarding long term holders
* Smart contracts must manually opt-in to earn yield. This allows the protocol to put more capital to work than would be otherwise possible.
* Smart strategies balance risk and reward more effectively than deploying capital in any single underlying strategy.

