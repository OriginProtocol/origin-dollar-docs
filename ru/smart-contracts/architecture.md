# Архитектура

![](../.gitbook/assets/ousd\_docs\_graphics\_3.png)

OUSD состоит из серии смарт-контрактов. Каждый из этих контрактов заключен в прокси-контракт, который можно усовершенствовать с помощью протоколов управления.

На внутреннем уровне доля владения в хранилище отслеживается с помощью рейтинговой системы, которая представляет процент доли владения в хранилище для каждого держателя. Контракт [ERC-20](api/erc-20-1.md) при просмотре баланса или инициировании перевода между кошельками выражает баланс в долларах США.

[Vault](api/vault.md) отвечает за производство и сжигание OUSD. Он также определяет процент активов, развернутых для каждой из поддерживаемых [стратегий](../core-concepts/supported-strategies/). Чтобы оптимизировать затраты на газ, в The Vault поддерживается буфер, позволяющий производить большинство депозитов и выкупов без ввода/вывода активов из стратегий.

The Flipper is a smart contract for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. This contract is used as an alternative way to route user transactions originating from the web app. It's important to note that this contract may become bankrupt on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Flipper uses around 45% less gas than Uniswap v3 due to its simplicity.

