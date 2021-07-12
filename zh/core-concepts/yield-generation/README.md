# 收益产生

**自动收益耕作**

虽然新兴的借贷和自动做市商池爆炸式地推动了总锁定价值 (TVL)，但同时产量农户想继续以高效，最优的方式手动分配资本，也变得越来越困难了。

[Yearn](https://yearn.finance/) 证明了智能合约可以将各种策略中的资金重新平衡自动化，以最佳方式赚取贷款利息，做市费和奖励代币。 Over time, new strategies will be deployed that maximize returns while minimizing risk and dependencies.

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

