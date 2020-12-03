# Генерирование дохода

**Автоматизированное получение прибыли**

"Кембрийский взрыв" новых кредитных и автоматизированных пулов маркет-мейкеров дал толчок к блокировке общей стоимости \(TVL\), однако он так же усложнил эффективное и оптимальное распределение капитала вручную лицам, занимающихся добычей прибыли.

[Yearn](https://yearn.finance/) продемонстрировал, что смарт-контракты могут автоматизировать ребалансировку средств по различным стратегиям, чтобы оптимально зарабатывать проценты по кредитам, комиссии за маркет-мейкинг и вознаграждения токенами. Over time, new strategies will be deployed that maximize returns while minimizing risk and dependencies.

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

