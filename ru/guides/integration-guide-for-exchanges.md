# Руководство по интеграции для бирж

Централизованные биржи будут играть важную роль в достижении нашей цели сделать OUSD повсеместно распространенным. Мы рады помочь любой бирже, которая хочет сделать OUSD доступным для своих пользователей. Мы считаем, что OUSD станет отличным дополнением к любой бирже, которая хочет предложить своим пользователям как превосходный стейблкоин, так и новую возможность получать высокий доход.

Эти документы - отличная отправная точка для понимания того, как работает OUSD. Вот несколько важных вопросов для бирж, которые хотят интегрировать OUSD:

**Вы хотите участвовать в получении дохода?**

Мы предполагаем, что ответ будет положительным, и мы также очень поощряем это! Однако, могут быть некоторые случаи, когда вы предпочтете действовать быстро и добавить на свою биржу OUSD, не участвуя в [процессе перераспределения OUSD](../core-concepts/elastic-supply/rebasing-and-smart-contracts.md), так как это является самой быстрой и простой интеграцией. Для бирж, которые хотят добавить токен OUSD, но ограничены в технических ресурсах, есть возможность сначала запустить версию без перераспределения, пока ваши специалисты вносят необходимые изменения. Чтобы запретить перераспределение OUSD, необходимо вызвать функцию `rebaseOptOut()` из каждого кошелька EOA, на котором хранится OUSD, или ничего не делать, если OUSD хранится на смарт-контрактах. OUSD без перераспределения абсолютно такой же, как и любой другой токен ERC-20.

**Балансы клиентов хранятся на смарт-контрактах (например, мульти-подписях) или в кошельках EOA?**

Любой смарт-контракт, содержащий OUSD, должен вручную предоставить согласие на получение дохода, вызывая функцию `rebaseOptIn()`. Это необходимость, вызванная [гибким предложением](../core-concepts/elastic-supply/) и [природой перераспределения OUSD](../core-concepts/elastic-supply/rebasing-and-smart-contracts.md). Многие биржи переводят средства клиентов на кошельки с мульти-подписями для холодного хранения. Делая это, Вам нужно убедиться, что было получено разрешение на перераспределение, чтобы не потерять заработок.

**Кешируете ли вы балансы пользователей?**

OUSD динамически обновляет значение, возвращаемое функцией `balanceOf()` в нашем контракте ERC20. Балансы пользователей будут обновляться несколько раз в день по мере того, как протокол генерирует новую доходность. Пока вы не кешируете это значение, пользователи всегда будут видеть правильную сумму OUSD, которую они держат.

**Вы объединяете средства пользователей?**

Если вы объединяете средства, вы должны быть уверены, что каждый пользователь получает пропорциональную сумму дохода, генерируемого протоколом. Probably the easiest way to do this is to track each user's balance as a percentage of a pool instead of as a fixed amount.

**What is your plan for liquidity?**

OUSD can be minted or redeemed at any time using the [Origin Dollar DApp](https://www.ousd.com), or directly from our smart contracts. If you are planning on providing liquidity yourself, you should be aware that the exact amount of OUSD you will receive in exchange for your USDT, USDC, or DAI depends on the current exchange rates as determined by the [oracles](../smart-contracts/api/oracle.md). If you are planning on redeeming OUSD for the underlying stablecoins, you should know there is a 0.5% exit fee and OUSD will return a basket of stable coins in proportion to the backing stablecoins in the pool. We encourage exchanges to leverage other pools of liquidity, such as on Uniswap, to avoid those fees. If possible, mints or redeems should be done in large batches for maximum efficiency. 



