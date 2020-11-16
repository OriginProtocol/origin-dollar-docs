# Как это работает

#### На 100% поддерживаемый и стабильный

Origin Dollar \(OUSD\) - это токен, соответствующий стандарту ERC-20 для сети Ethereum.

OUSD - это стабильная валюта, которая в соотношении 1:1 поддерживается другими стейблкоинами, такими как USDT, USDC и DAI. В результате 1 OUSD всегда должен быть очень близок к стоимости 1 USD.

{% hint style="success" %}
1 OUSD = 1 доллар США
{% endhint %}

#### "Чеканка" OUSD

Пользователи конвертируют свои существующие стейблкоины \ (в настоящее время USDT, USDC и DAI \) в OUSD в официальном [Origin Dollar DApp](www.ousd.com). Выпущенные OUSD немедленно начинают приносить доход от начисления сложных процентов.

**Вомещение OUSD**

Пользователи могут конвертировать свои OUSD в другие стейблкоины в любое время, используя [Origin Dollar DApp](www.ousd.com). A 0.5% exit fee is charged upon redemption and is distributed as additional yield to the remaining participants in the vault. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from syphoning stablecoins from the vault in the event of mispricings of of the underlying assets. Комиссия существует для того, чтобы заинтересовывать долгосрочных держателей, а не краткосрочных спекулянтов.

Смарт-контракт после выкупа определит, какой(-ие) стейблкоин (-ы) вернуть пользователю. In the current implementation, the vault will return coins in the same ratio as the current holdings. This lack of user optionality also protects the vault as a whole in the event that any of the supported stablecoins loses its peg to the dollar.

{% hint style="warning" %}
Существует **комиссия за выход 0,5%**, и пользователь не выбрает, какие стейблкоины он получит.
{% endhint %}

#### **Автоматизированное получение дохода**

OUSD генерирует доходность за счет задействования основных стейблкоинов, которые были внесены в качестве депозита в смарт-контракт OUSD в другие протоколы DeFi, такие как Compound, Aave, Uniswap, Balancer и Curve. It is expected there will be new diversified strategies added to the vault every month. Собранные проценты, торговые комиссии и токены вознаграждений объединяются и конвертируются в стейблкоины для получения доходности, номинированной в OUSD. Со временем протокол будет перемещать активы в различные пулы ликвидности и из них, чтобы обеспечить максимальную доходность для держателей OUSD.

#### **Гибкое предложение**

Сгенерированная прибыль передается держателям OUSD через постоянное перемещение денежной массы. OUSD постоянно корректирует денежную массу в соответствии с доходностью, генерируемой протоколом. Это позволяет цене OUSD оставаться на уровне 1 доллара США, в то время как остатки в кошельках держателей токенов корректируются в режиме реального времени, чтобы отражать доходность, полученную по протоколу.

Конечным результатом является стейблкоин, который автоматически приносит огромную прибыль, его легко портатить, но целесообразнее держать, чем существующие ныне стейблкоины.

