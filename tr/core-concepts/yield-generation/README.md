# Verim Üretimi

**Otomatik yield farming**

Yeni borç verme ve otomatikleştirilmiş piyasa yapıcı havuzlarındaki Kambriyen patlaması, kilitlenen toplam değeri \ (TVL \) beslerken, aynı zamanda verim çiftçilerinin sermayeyi verimli ve en uygun yollarla manuel olarak tahsis etmesini giderek daha zor hale getirdi.

[Yearn](https://yearn.finance/) has demonstrated that smart contracts can automate the rebalancing of funds across various strategies to optimally earn lending interest, market-making fees, and rewards tokens. Over time, new strategies will be deployed that maximize returns while minimizing risk and dependencies.

![Automated yield farming on the OUSD protocol](../../.gitbook/assets/ousd_earnings_graphic.png)

OUSD uses the following high-level strategies for generating yield:

{% page-ref page="lending.md" %}

{% page-ref page="market-making.md" %}

{% page-ref page="ödüller.md" %}

OUSD is able to generate higher yields than competing protocols due to a combination of important design decisions that amplify the rewards that are returned to OUSD holders:

* Exit fees are returned to the pool, rewarding long term holders
* Price oracles favor the collective over the individual, again rewarding long term holders
* Smart contracts must manually opt-in to earn yield. This allows the protocol to put more capital to work than would be otherwise possible.
* Smart strategies balance risk and reward more effectively than deploying capital in any single underlying strategy.

