# Приступая к работе

Эти документы предназначены для того, чтобы объяснить, как работает OUSD, сообщить о потенциальных рисках и преимуществах и предоставить руководство для разработчиков, которые хотят внести свой вклад в нашу кодовую базу или интегрировать OUSD в свои продукты. Вот несколько способов приступить к работе.

**"Чеканка" или Выкуп**

The OUSD Mint allows anyone to create or trade-in OUSD tokens using our [DApp](www.ousd.com) and a web-3 enabled cryptocurrency wallet like [Metamask](https://www.metamask.io). Это естественный способ получить OUSD, особенно если вам нужна крупная сумма, которая может привести к движению рынка на других биржах.

**Купить на биржах**

Для небольших сумм самый простой способ начать зарабатывать с помощью OUSD - купить его на бирже. Мы ожидаем, что OUSD скоро станет доступным на большом количестве децентрализованных и централизованных бирж.

Децентрализованные биржи:

* [Buy OUSD on 1inch](https://app.1inch.io/#/1/swap/USDT/OUSD)
* [Buy OUSD on Curve](https://curve.fi/factory/9)
* [Buy OUSD on Uniswap v3](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)
* [Buy OUSD on Uniswap v2](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86&use=v2)
* [Buy OUSD on Sushiswap](https://exchange.sushiswapclassic.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86)

Централизованные биржи:

* Buy OUSD on KuCoin
  * [OUSD/USDT](https://trade.kucoin.com/OUSD-USDT)
  * [OUSD/BTC](https://trade.kucoin.com/OUSD-BTC)
* Buy OUSD on Virgox
  * [OUSD/USDT](https://virgox.com/exchange/141)
* [Buy OUSD on Dharma App](https://www.dharma.io/) \(US only\)

**Добавить OUSD в Ваш кошелек**

{% hint style="success" %}
Основной адрес ERC20 для Origin Dollar \(OUSD \):   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

Если Ваш OUSD автоматически не отображается в Вашем кошельке, Вы сможете добавить его вручную, используя вышеуказанный адрес. Если вы планируете [хранить OUSD в кошельке с мульти-подписями](core-concepts/elastic-supply/rebasing-and-smart-contracts.md), убедитесь в возможности автоматически получать доход. Мы хотим, чтобы OUSD поддерживалось как можно большим количеством кошельков и включался в различные списки хорошо известных токенов. Мы будем очень признательны за любую помощь, которую Вы можете предложить в этой области.

**Интегрирование OUSD**

OUSD - это нестандартный токен ERC-20, который требует специальной интеграции для большинства приложений, которые хотят его поддерживать. В частности, разработчикам важно понимать, как работает наше гибкое предложение, поскольку это может легко вызвать неожиданный режим работы.

Если вы являетесь представителем разработчиков кошельков или криптовалютных бирж, которые заинтересованы в поддержке OUSD, обратитесь к следующим руководствам:

{% page-ref page="core-concepts/elastic-supply/rebasing-and-smart-contracts.md" %}

{% page-ref page="smart-contracts/architecture.md" %}

{% page-ref page="smart-contracts/api/" %}

**Аналитика для разработчиков**

Наша внутренняя панель инструментов для разработчиков доступна по адресу [analytics.ousd.com](https://analytics.ousd.com). На панели инструментов отображается текущее оборотное предложение, активы, находящиеся под управлением в хранилище, и текущее распределение между стейблкоинами и стратегиями.

**Помощь**

Присоединяйтесь к Origin Dollar\#engineering room\ на сервере Origin в [Discord](www.originprotocol.com/discord).  Наша команда и члены нашего сообщества с нетерпением ждут возможности помочь Вам в разработке. Ваши вопросы помогают нам стать лучше, поэтому не стесняйтесь спрашивать, если вы не можете найти здесь то, что ищете.

