# Права администратора

Смарт-контракты OUSD разработаны с возможностью улучшения владельцем. Команда Origin использует два разных контракта кошелька с мульти-подписями Gnosis для внесения изменений в протокол. Аудиты этих кошельков с мульти-подписями были проведены такими компаниями, как [OpenZeppelin](https://blog.openzeppelin.com/gnosis-multisig-wallet-audit-d702ff0e2b1e/), [ConsenSys Dilligence](https://blog.gnosis.pm/the-gnosis-multisig-wallet-and-our-commitment-to-security-ce9aca0d17f6), командой Origin и др.

{% hint style="info" %}
Задержка действий администратора дает пользователям возможность выхода из OUSD, если его администраторы станут злонамеренными, будут скомпрометированы или внесут изменения, которые не нравятся пользователям.
{% endhint %}

Основной администратор - это контракт с 5 из 8 подписей, которые требуются для внесения любых изменений кода в протоколе. OUSD можно обновить только из этого кошелька с 5 из 8 подписей. Ключи к этой мульти-подписке принадлежат лицам, имеющим тесные связи с компанией, и даже действующие вместе основатели Origin не обладают достаточным контролем, чтобы самостоятельно выполнять функции владельца. В дополнение, контракты OUSD подлежат [временной блокировке](../smart-contracts/api/timelock.md) что позволяет команде Origin продолжать вносить изменения в протокол, но только с задержкой во времени.

Некоторые функции, такие как перераспределение средств между стратегиями или приостановка депозитов, могут быть запущены без временной блокировки и с гораздо меньшим количеством подписей. Это позволяет команде Origin быстрее реагировать на рыночные условия или угрозы безопасности. Эти подписывающие стороны, известные как Стратеги, имеют возможность выполнять ограниченное количество функций __ только с 2 из 9 подписей.

Having these admin privileges is necessary in the early days to ensure that the protocol is secure and optimized for earning yields while minimizing risks. We expect to release multiple iterations of our smart contracts in the first several months of the protocol's existence.

Once several upgrade cycles have been completed, we intend to transfer ownership from our company control to a decentralized governance contract, thereby allowing the community to vote and participate in future protocol updates.

