# Временная блокировка

{% hint style="danger" %}
The timelock has been added but is currently set to 1 minute. This allows for a faster response if any critical issues are discovered. The timelock is governed by Origin's 5 of 8 multi-sig.
{% endhint %}

Контракт с временной блокировкой предусматривает 48-часовой период ожидания, прежде чем любые изменения в контрактах OUSD будут выполнены. Временная блокировка может быть вызвана нашим мульти-подписями, являющимися владельцами наших контрактов [ERC-20](../architecture.md), [Vault](vault.md)и [Strategies](strategies.md). Задержка действий администратора дает пользователям возможность выхода OUSD, если его администраторы станут злонамеренными, будут скомпрометированы или внесут изменения, которые не нравятся пользователям.

{% hint style="info" %}
Временная блокировка - это мера безопасности, которая дает держателям OUSD 48 часов, чтобы вывести свои средства, если у них есть возражения против любых предлагаемых обновлений протокола.
{% endhint %}

OUSD использует немного измененную версию [ Накапливаемой временной блокировки](https://compound.finance/docs/governance), которая была [проаудирована OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). The two notable differences are:

1. Первоначально OUSD будет использовать более короткий период ожидания \(48 часов\), чем Compound \(72 часа\), чтобы обеспечить более быстрый ответ в случае обнаружения каких-либо проблем.
2. Some actions, such a reallocating funds between existing strategies and freezing deposits can be called immediately without requiring the 48 waiting period. This is in case a major vulnerability is discovered.





