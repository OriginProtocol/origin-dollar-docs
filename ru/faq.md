# FAQ

**Где я могу купить OUSD?**

Ознакомьтесь с разделом [Приступая к работе](https://docs.ousd.com/getting-started) чтобы увидеть множество вариантов.

**Каковы затраты на создание и выкуп OUSD?**

Как и в случае любой транзакции Ethereum, Вам понадобится эфир для взаимодействия со смарт-контрактом OUSD. Мы приняли меры по сокращению использования газа, где это было возможно, но эти расходы могут варьироваться.

Каждый раз, когда Вы создаете или выкупаете OUSD, к Вашим депонированным или выведенным стейблкоинам будет применяться обменный курс. Вы можете узнать больше об этом в разделе [Ценовые Оракулы](https://docs.ousd.com/core-concepts/price-oracles).

Чтобы стимулировать долгосрочное хранение OUSD и защитить протокол от злоумышленников, со всех выкупов взимается комиссия за выход в размере 0,5%. Вы можете узнать больше об этом в разделе [Как это работает](https://docs.ousd.com/how-it-works).

**Как скоро мой баланс увеличится, если у меня будет OUSD?**

Сумма OUSD в вашем кошельке будет расти каждый раз, когда происходит положительное событие перераспределения. Вы можете узнать больше об этом в разделе [Гибкое предложение](https://docs.ousd.com/core-concepts/elastic-supply). В настоящее время предложение перераспределяется несколько раз в день и обычно зависит от того, как много людей создают и выкупают OUSD.

**Почему не растет OUSD, если он хранится в Uniswap, SushiSwap и т.д.?**

По умолчанию события перераспределения не влияют на предложение OUSD, которое находится в смарт-контрактах. Эти контракты могут получить дополнительных OUSD, если они способны работать с токенами эластичного предложения. Вы можете прочитать больше об этом в разделе [Перераспределение & Смарт-Контракты](https://docs.ousd.com/core-concepts/elastic-supply/rebasing-and-smart-contracts).

**За счет чего возможен такой высокий APY?**

Вы можете прочитать о наших различных стратегиях в разделе [Генерирование дохода](https://docs.ousd.com/core-concepts/yield-generation). В настоящее время мы получаем большую часть дохода от сбора токенов вознаграждений \(а именно COMP и CRV\). Additionally, the yield increases as more OUSD is held in smart contracts that do not opt into rebasing since the underlying collateral continues to earn for the average OUSD holder.

**Why is my balance increasing at a slower rate than the advertised APY?**

OUSD balances increase when the supply is rebased. But the size of each rebase varies wildly depending on how much the vault has earned since the last rebase. And while most rebases collect a small amount earnings from lending strategies, other rebases involve liquidating rewards tokens or collecting fees. As a result, the yield will vary significantly during short time periods.

**What about the hack? Is OUSD safe?**

On November 7th 2020, OUSD was exploited for 7M USD due to a previously undetected reentrancy bug. You can read more [details about the hack](https://medium.com/originprotocol/urgent-ousd-has-hacked-and-there-has-been-a-loss-of-funds-7b8c4a7d534c) on our blog as well as the [detailed compensation plan](https://medium.com/originprotocol/origin-dollar-ousd-detailed-compensation-plan-faa73f87442e) for taking care of the affected users. Origin Dollar was relaunched in December after completing multiple audits and security upgrades. You can learn more about the steps taken to secure the protocol in our [relaunch announcement](https://medium.com/originprotocol/origin-dollar-ousd-is-back-b8ee0c601dad).

