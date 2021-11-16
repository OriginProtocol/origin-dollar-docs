# Гибкое предложение

**Гибкое предложение. Стабильная цена.**

OUSD работает не так, как большинство токенов. Instead of the price increasing as the value of the assets under management increase (as with Compound cTokens or Yearn yTokens), the value of one OUSD remains constant at approximately $1. Instead, the contracts constantly adjust the monetary supply and automatically updates the balance in every token holder’s wallet to reflect the yield that has been earned by the protocol.&#x20;

{% hint style="info" %}
Думайте об этом как о процентах, начисляемых на ваш банковский счет. Расчетная единица и стоимость доллара США не меняются. Вы просто получаете больше долларов США со временем, зарабатывая проценты.
{% endhint %}

![](../../.gitbook/assets/ousd\_docs\_graphics\_4.png)

This mechanism was inspired by the novel approach taken by [Ampleforth](https://www.ampleforth.org), but there are some key differences that are worth highlighting:

1. OUSD на 100% обеспечен другими стейблкоинами и не имеет такой же проблемы с поддержанием привязки к доллару. Given the ease of minting and redeeming OUSD, we can count on arbitrageurs to ensure the peg is maintained.&#x20;
2. Перераспределение OUSD будет только увеличивать предложение, поскольку количество вновь созданных OUSD привязано к реализованной прибыли, полученной с помощью лежащих в основе стратегий. Ваш основной капитал защищен до тех пор, пока все в порядке с основными протоколами кредитования/AMM и протоколами стейблкоинов. Ваш баланс OUSD никогда не уменьшится, но его стоимость может упасть, если произойдет сбой в основных системах.
3. Unlike Ampleforth, which only rebases once a day, the monetary supply of OUSD is constantly being updated in real-time as yield is generated. Перераспределение запускается регулярно, когда пользователи взаимодействуют с контрактами OUSD. Chainlink Keepers ensure at least one rebase occurs every day.

**Запуск перераспределения вручную**

Кто угодно в любой момент может запустить перераспределние, [вызвав функцию перераспределения в хранилище](https://etherscan.io/address/originvault.eth#writeProxyContract). Вы можете сделать это в Etherscan, подключив кошелек web3.
