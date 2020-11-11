# Гибкое предложение

**Гибкое предложение. Стабильная цена.**

OUSD работает не так, как большинство токенов. Вместо увеличения цены по мере увеличения стоимости активов под управлением (как в случае с Compound cTokens или Yearn yTokens), стоимость одного OUSD остается постоянной и составляет примерно 1 доллар США. Вместо этого контракты постоянно корректируют денежную массу и автоматически обновляют баланс в кошельке каждого держателя токенов, чтобы отразить доход, полученный протоколом.

{% hint style="info" %}
Думайте об этом как о процентах, начисляемых на ваш банковский счет. Расчетная единица и стоимость доллара США не меняются. Вы просто получаете больше долларов США со временем, зарабатывая проценты.
{% endhint %}

![](../../.gitbook/assets/ousd_docs_graphics_4.png)

Этот механизм был вдохновлен новым подходом, принятым [Ampleforth](https://www.ampleforth.org/), но есть некоторые ключевые отличия, которые стоит выделить:

1. OUSD is 100% backed by other stablecoins and does not have the same challenge maintaining the peg to the dollar. Учитывая простоту создания и выкупа OUSD, мы можем рассчитывать на арбитражеров, которые обеспечат поддержание привязки.
2. OUSD rebasing will only increase supply since the amount of OUSD minted is tied to the realized gains earned by the underlying strategies. Your principal is protected as long as nothing goes wrong with the underlying lending/AMM and stablecoin protocols. Your OUSD balance will never decrease, but the value could drop if there's a failure in the underlying systems.
3. Unlike Ampleforth, which rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Rebases are triggered regularly as users interact with the OUSD contracts.

**Manually triggering a rebase**

Anyone can trigger a rebase at any time by [calling the rebase function on the vault](https://etherscan.io/address/originvault.eth#writeProxyContract). You can do this on Etherscan by connecting a web3 wallet.

