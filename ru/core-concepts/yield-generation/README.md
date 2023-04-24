# Генерирование дохода

**Автоматизированное получение прибыли**

While the Cambrian explosion of new lending and automated market maker pools has fueled total value locked (TVL), it has also made it increasingly challenging for yield farmers to manually allocate capital in efficient and optimal ways.

[Yearn](https://yearn.finance) has demonstrated that smart contracts can automate the rebalancing of funds across various strategies to optimally earn lending interest, market-making fees, and rewards tokens. Со временем будут внедрены новые стратегии, которые увеличивают прибыль при минимизации рисков и зависимостей.

![Automated yield farming on the OUSD protocol](../../.gitbook/assets/ousd_earnings_graphic.png)

OUSD использует следующие высокоуровневые стратегии для получения дохода:

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

* Плата за выход возвращается в пул, вознаграждая долгосрочных держателей
* Ценовые оракулы предпочитают группу, а не отдельного человека, опять же, вознаграждая долгосрочных владельцев
* Чтобы получать доход, смарт-контракты необходимо подписывать вручную. Это позволяет протоколу задействовать больше капитала, чем это было бы возможно в противном случае.
* Умные стратегии уравновешивают риск и вознаграждение более эффективно, чем вложение капитала в любую одну базовую стратегию.
