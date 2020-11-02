# 弹性供应

**弹性供应。 价格稳定。**

OUSD 与大多数代币的运作方式不同。 与 Compound cToken 或 Yearn yTokens 不一样的是，一个 OUSD 的价值保持在大约 1 美元。 合余额不断调整货币供应量，并自动更新每个代币持有者钱包中的余额，以反映协议所赚取的收益。

{% hint style="info" %}
您可以将其视为银行帐户中的利息。 美元的帐户单位和价值不变。 当您赚取利息时，您将获得更多美元。
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

这个机制的灵感来自于 [Ampleforth](https://www.ampleforth.org/)，但是也有一些重要的区别值得强调：

1. OUSD 100％ 由其他稳定币支持，在保持与美元挂钩方面不会遇到相同的挑战。 由于 OUSD 的发行和赎回很容易，我们可以依靠套利者来确保OUSD, 钉住美元。
2. OUSD rebasing should only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. 只要基础贷款 / AMM和稳定币协议没有任何问题，您的资金就会受到保护。 Any decrease in your balance would be an indication of trouble in the system.
3. 不像 Ampleforth 每天重新平衡的机制，OUSD 的货币供应随着收益的产生而持续地实时更新。

