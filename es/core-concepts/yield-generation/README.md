# Generación de rendimiento

**Cultivo de Rendimiento Automatizado**

While the Cambrian explosion of new lending and automated market maker pools has fueled total value locked (TVL), it has also made it increasingly challenging for yield farmers to manually allocate capital in efficient and optimal ways.

[Yearn](https://yearn.finance) has demonstrated that smart contracts can automate the rebalancing of funds across various strategies to optimally earn lending interest, market-making fees, and rewards tokens. Con el tiempo, se implementarán nuevas estrategias que maximizan los retornos y minimizan el riesgo y las dependencias.

![Recolección de rendimiento automatizada en el protocolo OUSD](../../.gitbook/assets/ousd_earnings_graphic.png)

OUSD utiliza las siguientes estrategias de alto nivel para generar rendimiento:

{% content-ref url="lending.md" %}
[lending.md](lending.md)
{% endcontent-ref %}

{% content-ref url="market-making.md" %}
[market-making.md](market-making.md)
{% endcontent-ref %}

{% content-ref url="rewards.md" %}
[rewards.md](rewards.md)
{% endcontent-ref %}

OUSD is able to generate higher yields than competing protocols due to a combination of important design decisions that amplify the rewards that are returned to OUSD holders:

* Las tarifas de salida se devuelven al grupo de liquidez, recompensando a los holders a largo plazo
* Los oráculos de precios favorecen al colectivo sobre el individual, recompensando nuevamente a los holders a largo plazo
* Los contratos inteligentes deben optar manualmente para obtener rendimiento. Esto permite que el protocolo ponga más capital a trabajar de lo que sería posible de otra manera.
* Las estrategias inteligentes equilibran el riesgo y la recompensa de manera más eficaz que la implementación de capital en una sola estrategia subyacente.
